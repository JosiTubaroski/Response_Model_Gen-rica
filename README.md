<div> 
<p><a href="https://github.com/JosiTubaroski/Controllers_Services/blob/main/README.md">Home</a></p>
</div> 

# ResponseModel

### Criando a ResponseModel.cs, que é a nossa Resposta Modelo.

<img src="https://github.com/JosiTubaroski/Controllers_Services/blob/main/img/02_Response_Model.png"/>

#### Detalhes do código.

https://github.com/JosiTubaroski/Controllers_Services/blob/main/img/ResponseModel.cs

Esse código define uma <b>classe genérica</b> chamada ResponseModel<T> dentro do namespace WebAPI8_Video.Models. Essa classe é usada para estruturar respostas padronizadas em uma API. Vamos detalhar parte por parte:

### 1️⃣ Namespace e Importação

<img src="https://github.com/JosiTubaroski/Controllers_Services/blob/main/img/03_Inicio_Response.png"/>

- O namespace WebAPI8_Video.Models indica que essa classe pertence ao conjunto de modelos do projeto.
- A linha using WebAPI8_Video.Migrations; sugere que esse projeto contém migrations (alterações estruturais no banco de dados), mas essa importação não está sendo usada dentro dessa classe específica.

### 2️⃣ Definição da Classe Genérica

<img src="https://github.com/JosiTubaroski/Controllers_Services/blob/main/img/04_PublicClass_Response.png"/>

- ResponseModel<T> é uma <b>classe genérica</b>, onde <T> representa um <b>tipo genérico.</b>
- Isso significa que ResponseModel pode ser usada para diferentes tipos de dados, como ResponseModel<string>, ResponseModel<int>, ou até mesmo ResponseModel<Usuario>.

 ### 3️⃣ Propriedades da Classe

 <img src="https://github.com/JosiTubaroski/Controllers_Services/blob/main/img/04_Propriedade_Response.png"/>

 - Dados: Armazena a informação principal da resposta. O tipo é genérico (T?), então pode conter qualquer tipo de dado.
 - O ? (nullable) indica que Dados pode ser null.

 <img src="https://github.com/JosiTubaroski/Controllers_Services/blob/main/img/05_String_Response.png"/>

 - Mensagem: Campo usado para armazenar uma mensagem descritiva da resposta, como "Operação realizada com sucesso" ou "Erro ao processar requisição".
 - O valor padrão é string vazia (string.Empty).

  <img src="https://github.com/JosiTubaroski/Controllers_Services/blob/main/img/06_Response_True.png"/>

  - Status: Representa o sucesso (true) ou falha (false) da operação.
  - O valor padrão é true, assumindo que a maioria das respostas serão bem-sucedidas.

 ### 4️⃣ Exemplo de Uso

Vamos supor que essa classe seja usada em uma API para responder a uma requisição de login.

<img src="https://github.com/JosiTubaroski/Controllers_Services/blob/main/img/07_Response_Sucesso.png"/>

## Conclusão

A classe ResponseModel<T> é uma estrutura de resposta padronizada que melhora a <b>organização e legibilidade</b> da API. Ela permite que diferentes endpoints retornem respostas uniformes, tornando o consumo de API mais previsível e consistente.
