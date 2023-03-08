# nas configuracoes de PHP, qual a diferença entre post_max_size upload_max_filesize?

Em configurações do PHP, "post_max_size" e "upload_max_filesize" são duas diretivas diferentes que controlam o tamanho máximo de dados que podem ser enviados para um script PHP via método POST e via upload de arquivos, respectivamente.

A diretiva "post_max_size" define o tamanho máximo de dados que podem ser enviados para um script PHP através do método POST. Isso inclui o tamanho de todos os campos do formulário, bem como de quaisquer arquivos que estejam sendo enviados. Se o tamanho dos dados enviados exceder o valor especificado em "post_max_size", o PHP interromperá o processamento do script e retornará um erro.

Já a diretiva "upload_max_filesize" define o tamanho máximo de arquivos que podem ser enviados via upload para um script PHP. Se o tamanho de um arquivo enviado exceder o valor especificado em "upload_max_filesize", o PHP interromperá o upload do arquivo e retornará um erro.

Em resumo, a diferença entre as duas diretivas é que "post_max_size" controla o tamanho total dos dados enviados via método POST, enquanto "upload_max_filesize" controla o tamanho máximo de arquivos enviados via upload. No entanto, é importante notar que ambos os valores devem ser definidos adequadamente para permitir que os usuários enviem dados e arquivos de tamanho apropriado para o seu aplicativo ou website.

#### Supondo que tenho 3 arquivos de 5MB, qual diretiva devo alterar para ser aceito esses 3 arquivos que somados são 15MB

Para permitir o envio de arquivos de até 15MB (ou qualquer tamanho que você precise) via upload em um script PHP, você precisa alterar a diretiva "upload_max_filesize" para um valor igual ou maior que 15MB.

Se você tem três arquivos de 5MB cada um, o tamanho total dos três arquivos será de 15MB. Isso significa que, se você quiser permitir o upload desses três arquivos, precisará definir "upload_max_filesize" como pelo menos 15MB.

Lembre-se também de que a diretiva "post_max_size" deve ser maior ou igual à diretiva "upload_max_filesize", pois ela define o tamanho máximo total dos dados enviados via método POST, incluindo o tamanho dos arquivos enviados via upload. Então, se você aumentar o valor de "upload_max_filesize", verifique se o valor de "post_max_size" também está ajustado adequadamente para o seu caso de uso.

```
post_max_size:        Deve ser maior ou igual à diretiva "upload_max_filesize", pois ela define o tamanho máximo total dos dados enviados via método POST
upload_max_filesize:  Define o tamanho máximo de arquivos que podem ser enviados via upload
```
