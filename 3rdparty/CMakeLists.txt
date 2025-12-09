# macro para configurar o uso da versão local ou do sistema de um pacote
# Usa:
#	HAVE_LOCAL_${name} - a versão local está disponível?
#	${name}_LOCAL_LIBRARIES - bibliotecas da versão local
#	${name}_LOCAL_INCLUDE_DIRS - diretórios de include da versão local
#	HAVE_SYSTEM_${name} - a versão do sistema está disponível?
#	${name}_SYSTEM_LIBRARIES - bibliotecas da versão do sistema
#	${name}_SYSTEM_INCLUDE_DIRS - diretórios de include da versão do sistema
# Gera:
#	WITH_LOCAL_${name} - usar a versão local do pacote (somente quando local está disponível)
#	WITH_${name} - usar este pacote
#	${name}_LIBRARIES - bibliotecas
#	${name}_INCLUDE_DIRS - diretórios de include
macro( CONFIGURE_WITH_LOCAL_OR_SYSTEM name )
	unset( ${name}_LIBRARIES CACHE )
	unset( ${name}_INCLUDE_DIRS CACHE )
	if( HAVE_LOCAL_${name} )
		set( WITH_LOCAL_${name} ON
			CACHE BOOL "usar versão local de ${name}" )
	else()
		unset( WITH_LOCAL_${name} CACHE )
	endif()
	if( WITH_LOCAL_${name} )
		message( STATUS "Configurando para ${name} local" )
		set( ${name}_LIBRARIES ${${name}_LOCAL_LIBRARIES} )
		set( ${name}_INCLUDE_DIRS ${${name}_LOCAL_INCLUDE_DIRS} )
		message( STATUS "Configurando para ${name} local - concluído" )
	elseif( HAVE_SYSTEM_${name} )
		message( STATUS "Configurando para ${name} do sistema" )
		set( ${name}_LIBRARIES ${${name}_SYSTEM_LIBRARIES} )
		set( ${name}_INCLUDE_DIRS ${${name}_SYSTEM_INCLUDE_DIRS} )
		message( STATUS "Configurando para ${name} do sistema - concluído" )
	endif()
	if( WITH_LOCAL_${name} OR HAVE_SYSTEM_${name} )
		set( WITH_${name} ON
			CACHE BOOL "usar ${name}" )
	else()
		unset( WITH_${name} CACHE )
	endif()
	set( ${name}_LIBRARIES ${${name}_LIBRARIES}
		CACHE PATH "bibliotecas ${name}" )
	set( ${name}_INCLUDE_DIRS ${${name}_INCLUDE_DIRS}
		CACHE PATH "diretórios de include ${name}" )
	mark_as_advanced( ${name}_LIBRARIES )
	mark_as_advanced( ${name}_INCLUDE_DIRS )
endmacro( CONFIGURE_WITH_LOCAL_OR_SYSTEM )


add_subdirectory( httplib )
add_subdirectory( json )
add_subdirectory( libconfig )
add_subdirectory( mysql )
add_subdirectory( pcre )
add_subdirectory( rapidyaml )
add_subdirectory( yaml-cpp )
add_subdirectory( zlib )