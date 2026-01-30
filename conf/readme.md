# Diretórios de Importação

## Para que serve o diretório import?

O diretório `import/` fornece uma forma de você alterar suas configurações sem precisar nem tocar nos arquivos principais `/conf/` e `/db/`.

Ao colocar suas entradas personalizadas dentro do diretório `import/` nessas duas localizações, seus arquivos centrais não terão conflitos quando você atualizar o servidor. Você guarda apenas suas alterações, e o resto é atualizado pelo rAthena.

## Como isso funciona?

Pense em "import" como "sobrescrever". Coloque apenas as configurações que você modificou nos arquivos de importação, ou seja, apenas as configurações que você está substituindo.

Por exemplo, ao configurar um servidor, sempre existem algumas opções que os usuários querem mudar para que o rAthena se adapte às suas necessidades. O exemplo a seguir mostra como usar corretamente o diretório `/conf/import/`.  
(para exemplos de `/db/import/`, veja [/db/readme.md](/db/readme.md))

---

### Servidor de Login
---
Queremos usar senhas MD5 e desativar os métodos de criação de conta `_m/f`.

#### /conf/import/login_conf.txt

```
new_account: no
use_MD5_passwords: yes
```

---

### Servidor de Personagens (Char Server)
---
Queremos mudar o nome do servidor para "Odin".

#### /conf/import/char_conf.txt

```
server_name: Odin
```

---

### Servidor de Mapas (Map Server)
---
Queremos esconder todas as mensagens de erro e adicionar alguns mapas personalizados.

#### /conf/import/map_conf.txt

```
// Torna a saída do servidor mais silenciosa, omitindo certos tipos de mensagens:
//16: Ocultar mensagens de Erro e Erro SQL.
console_silent: 16
map: 1@toy
map: 1@valley
map: shops
```

---

### Servidor Intermediário (Inter Server)
---
Queremos usar tabelas MySQL em vez de arquivos .txt.

#### /conf/import/inter_conf.txt

```
use_sql_db: yes
```

---

### Configurações de Log
---
Queremos registrar todos os itens e todas as mensagens de chat.

#### /conf/import/log_conf.txt

```
log_filter: 1
// Log de CHAT (Global, Sussurro, Grupo, Guilda, Chat principal, Clã) (Nota 3)
// log_chat: 63 = registra tudo
log_chat: 63
```

---

### Configurações de Batalha
---
Queremos alterar a forma como várias mecânicas funcionam. Tudo o que normalmente seria configurado no diretório `/conf/battle/` deve ir para `import/battle_conf.txt`.

Para ajudar a identificar de qual arquivo cada configuração veio, geralmente é uma boa ideia comentar o nome do arquivo original de onde aquele conjunto de configurações foi retirado.

#### /conf/import/battle_conf.txt

```
// guild.conf
guild_exp_limit: 90

// items.conf
vending_over_max: no
vending_tax: 100
weapon_produce_rate: 200
potion_produce_rate: 200
produce_item_name_input: 0x03

// misc.conf
duel_time_interval: 2
at_mapflag: yes
at_monsterignore: yes
cashshop_show_points: yes
hide_fav_sell: yes
// Define se o status da caixa de correio é exibido ao logar.
// Padrão: 0
// 0 = Não
// 1 = Sim
// 2 = Sim, quando houver cartas não lidas
mail_show_status: 2

// monster.conf
show_mob_info: 3

// party.conf
party_hp_mode: 1
display_party_name: yes

// pet.conf
pet_rename: yes

// player.conf
max_aspd: 196
max_third_aspd: 196
max_extended_aspd: 196
vip_disp_rate: no

// status.conf
debuff_on_logout: 3
```

---

Não podemos enfatizar o suficiente o quanto esse sistema é útil para todos.  
A maioria dos conflitos de git simplesmente deixará de existir se os usuários utilizarem corretamente o sistema `import/`.
