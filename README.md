## Tools
   - DB GUI Softwares
      - https://www.adminer.org/
      - https://www.sequelpro.com/
      - https://robomongo.org/
      - https://sqlectron.github.io/
      - https://eggerapps.at/postico/
   - CLI
      - https://linuxjourney.com/
   - Dumps/Backups
      - https://freek.dev/389-a-package-to-dump-your-database


### SQL Languages

**DDL** is short name of Data Definition Language, which deals with database schemas and descriptions, of how the data should reside in the database.

**DML** is short name of Data Manipulation Language which deals with data manipulation, and includes most common SQL statements such SELECT, INSERT, UPDATE, DELETE etc, and it is used to store, modify, retrieve, delete and update data in database.

**DCL** is short name of Data Control Language which includes commands such as GRANT, and mostly concerned with rights, permissions and other controls of the database system.

### **ACID** 

- Vem do acrônimo de Atomicidade, Consistência, Isolamento e Durabilidade. 

**Atomicidade**: É o que trata a transação efetuada. Veja, caso a transação tenha sido efetuada com sucesso, o valor será alterado/incluído na base de uma forma correta. Caso ocorra algum erro e a mesma tenha sido abortada, a base não deve receber esta alteração “pela metade”.

**Consistência**: Este garante que o processo da transação respeite todas as normas pré estabelecidas na integridade dos dados, como o relacionamento entre chaves, a fim de que não ocorra nenhuma divergência no momento da transação.

**Isolamento**: Uma das propriedades mais interessantes, o isolamento é uma garantia do dado verídico, ou seja, ele garante que uma transação sendo executada agora, não seja sobreposta por outras no mesmo campo.

**Durabilidade**: Este garante a integridade do dado já inserido na base. Sendo mais objetivo, este garante que qualquer alteração feita com sucesso deve permanecer no banco até uma nova intervenção.

### Datatypes
Text types

| Data type        | Description                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CHAR(size)       | Holds a fixed length string (can contain letters, numbers, and special characters). The fixed size is specified in parenthesis. Can store up to 255 characters                                                                                                                                   |
| VARCHAR(size)    | Holds a variable length string (can contain letters, numbers, and special characters). The maximum size is specified in parenthesis. Can store up to 255 characters. Note: If you put a greater value than 255 it will be converted to a TEXT type                                               |
| TINYTEXT         | Holds a string with a maximum length of 255 characters                                                                                                                                                                                                                                           |
| TEXT             | Holds a string with a maximum length of 65,535 characters                                                                                                                                                                                                                                        |
| BLOB             | For BLOBs (Binary Large OBjects). Holds up to 65,535 bytes of data                                                                                                                                                                                                                               |
| MEDIUMTEXT       | Holds a string with a maximum length of 16,777,215 characters                                                                                                                                                                                                                                    |
| MEDIUMBLOB       | For BLOBs (Binary Large OBjects). Holds up to 16,777,215 bytes of data                                                                                                                                                                                                                           |
| LONGTEXT         | Holds a string with a maximum length of 4,294,967,295 characters                                                                                                                                                                                                                                 |
| LONGBLOB         | For BLOBs (Binary Large OBjects). Holds up to 4,294,967,295 bytes of data                                                                                                                                                                                                                        |
| ENUM(x,y,z,etc.) | Let you enter a list of possible values. You can list up to 65535 values in an ENUM list. If a value is inserted that is not in the list, a blank value will be inserted.Note: The values are sorted in the order you enter them.You enter the possible values in this format: ENUM('X','Y','Z') |
| SET              | Similar to ENUM except that SET may contain up to 64 list items and can store more than one choice                                                                                                                                                                                               |

Number types

| Data type       | Description                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TINYINT(size)   | -128 to 127 normal. 0 to 255 UNSIGNED*. The maximum number of digits may be specified in parenthesis                                                                                                                                  |
| SMALLINT(size)  | -32768 to 32767 normal. 0 to 65535 UNSIGNED*. The maximum number of digits may be specified in parenthesis                                                                                                                            |
| MEDIUMINT(size) | -8388608 to 8388607 normal. 0 to 16777215 UNSIGNED*. The maximum number of digits may be specified in parenthesis                                                                                                                     |
| INT(size)       | -2147483648 to 2147483647 normal. 0 to 4294967295 UNSIGNED*. The maximum number of digits may be specified in parenthesis                                                                                                             |
| BIGINT(size)    | -9223372036854775808 to 9223372036854775807 normal. 0 to 18446744073709551615 UNSIGNED*. The maximum number of digits may be specified in parenthesis                                                                                 |
| FLOAT(size,d)   | A small number with a floating decimal point. The maximum number of digits may be specified in the size parameter. The maximum number of digits to the right of the decimal point is specified in the d parameter                     |
| DOUBLE(size,d)  | A large number with a floating decimal point. The maximum number of digits may be specified in the size parameter. The maximum number of digits to the right of the decimal point is specified in the d parameter                     |
| DECIMAL(size,d) | A DOUBLE stored as a string , allowing for a fixed decimal point. The maximum number of digits may be specified in the size parameter. The maximum number of digits to the right of the decimal point is specified in the d parameter |

Date types

| Data type   | Description                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DATE()      | A date. Format: YYYY-MM-DDNote: The supported range is from '1000-01-01' to '9999-12-31'                                                                                                                                                 |
| DATETIME()  | *A date and time combination. Format: YYYY-MM-DD HH:MI:SSNote: The supported range is from '1000-01-01 00:00:00' to '9999-12-31 23:59:59'                                                                                                |
| TIMESTAMP() | *A timestamp. TIMESTAMP values are stored as the number of seconds since the Unix epoch ('1970-01-01 00:00:00' UTC). Format: YYYY-MM-DD HH:MI:SSNote: The supported range is from '1970-01-01 00:00:01' UTC to '2038-01-09 03:14:07' UTC |
| TIME()      | A time. Format: HH:MI:SSNote: The supported range is from '-838:59:59' to '838:59:59'                                                                                                                                                    |
| YEAR()      | A year in two-digit or four-digit format.Note: Values allowed in four-digit format: 1901 to 2155. Values allowed in two-digit format: 70 to 69, representing years from 1970 to 2069                                                     |


![](https://user-images.githubusercontent.com/19540357/65278347-7b417c80-db1b-11e9-825d-280605deaccc.png)