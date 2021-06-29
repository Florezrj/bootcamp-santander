# O que é o arquivo postgresql.conf

## **Definição**

- ### Arquivo onde estão definidas e armazenadas todas as configurações do servidor **PostgreSQL.**

- ### _Alguns parâmetros só podem ser alterados com uma **reinicialização** do banco de dados._

- ### _A view pg_settings, acessada por dentro do banco de dados, guarda todas as configurações atuais._
#
#### _Localização do arquivo postgresql.conf_
##### POR PADRÃO EM PGDATA
#

## **Configurações de conexão**

- ### LISTEN_ADDRESSES
#### _Endereço(s) TCP/IP das interfaces que o servidor PostgreSQL vai escutar/liberar conexôes._

- ### PORT
#### _A PORTA tcp QUE O SERVIDOR pOSTGREsql VAI OUVIR. o PADRÃO É 5432._

- ### MAX_CONNECTIONS
#### _Número máximo de conexôes simultâneas no servidor PostgreSQL._

- ### SUPERUSER_RESERVED_CONNECTIONS
  #### _Numero de conexôes (slots) reservadas para conexôes de super usuario _

## **Configurações de Autenticação**

- ### AUTHENTICATION_TIMEOUT
#
- ### PASSWORD_ENCRYPTION
#
- ### SSL
#
  
## __Configurações de Mamória__

- ### SHARED_BUFFERS
- ### WORK_MEM
- ### MAINTENANCE_WORK_MEM

&nbsp;
# O arquivo ph_hba.conf

## **Definição**

> ### _Arquivo responsável pelo controle de autenticação dos usarios no servidor PostgreSQL._

&nbsp;
## **Métodos de Autenticação**
- ### TRUSTE (_conexão sem requisição de senha_)
- ### REJECT (_rejeitar Conexões_)
- ### MD5 (_criptografia md5_)
- ### PASSWORD (_senha sem criptografia_)
- ### GSS (_generic security support service application program interface_)
- ### SSPI (_security support provider interface - somenta para Windows_)
- ### KRB5 (_Kerberos V5_)
- ### IDENT (utiliza o usuário do sistema operacional do cliente via ident server)
- ### PEER (_utiliza o usuário do sistema operacional do cliente_)
- ### LDAP (_ldap server_)
- ### RADIUS (_radius server_)
- ### CERT (_auntenticação via certificado do ssl do cliente_)
- ### PAM (_Pluggable authentication modules. O usuario precisa estar no banco de dados_) 


# __O arquivo pg_ident.conf__

## Definição
> ### _Arquivo responsável por mapear os usuários do sistema operacional com os usuários do banco de dados._
 
&nbsp;

> ### _Localizado no diretório de dados PGDATA de sua instalação._
 
&nbsp;

> ### _A opção ident deve ser utilizada no arquivo de pg_hba.conf_

&nbsp;

# __Comandos Administrativos__

## __Ubuntu:__

- ### **pg_lsclusters**
> ### Lista todos os clusters PostgreSQL
- ### **pg_createcluster (version) (cluster name)**
> ### Cria um novo cluster PostgreSQL
- ### **pg_dropcluster (version) (cluster)**
> ### Apaga um cluster PostgreSQL
- ### pg-ctlcluster (version) (cluster) (action)
> ### start, stop, status, restart de clusters PostfresSQL

