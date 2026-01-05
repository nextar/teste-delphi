O desafio consiste em, através de requisições HTTPS e/ou conexão com o serviço de storage do AWS S3 (desejável), desenvolver uma aplicação capaz de buscar, armazenar e comparar diferenças entre os registros.
Você deverá consumir os dados das URLs disponibilizadas abaixo, tratar e armazenar os dados em um banco de dados da sua escolha.  


#### Urls para as requisições iniciais:
```https://teste-dev-delphi.s3.sa-east-1.amazonaws.com/people/C106C747-B7E6-42BC-98E9-618ECDE37EB0.json```    
```https://teste-dev-delphi.s3.sa-east-1.amazonaws.com/people/0FF1D11B-C43B-4D7A-97A3-0357D7896945.json```   
```https://teste-dev-delphi.s3.sa-east-1.amazonaws.com/people/7B293DE1-EF13-4659-A2BE-F5593A53D9A4.json```   
```https://teste-dev-delphi.s3.sa-east-1.amazonaws.com/people/49CAB937-5445-4E07-AAC7-EAE4FB4020B9.json```    
```https://teste-dev-delphi.s3.sa-east-1.amazonaws.com/people/0341197D-8DCD-445C-8C04-7CB78EF2013B.json```

    
Observe que cada JSON contém uma propriedade PHOTO, conforme exemplo abaixo e essa propriedade indica dois possíveis caminhos para obter o arquivo de imagem. 

-   Endereço de um bucket do S3 e o nome de um arquivo presente no mesmo, você deverá conectar no S3 usando as credenciais disponibilizadas, baixar os arquivos e persistir na base de dados.

-   Endereço de um arquivo público para realizar a requisição e obter o stream via HTTPS, baixar os arquivos e persistir na base de dados. 

Qualquer uma das escolhas acima é válida para a avaliação do teste.
```
{
    "uid": "{0FF1D11B-C43B-4D7A-97A3-0357D7896945}",
    "name": "Maria",
    "age": 22,
    "gender": "F",
    "phone": "+55 14 77777-7777",
    "photo": {
        "s3": {
            "path": "/images/",
            "filename": "0FF1D11B-C43B-4D7A-97A3-0357D7896945.png"
        },
        "https": {
            "url": "https://teste-dev-delphi.s3.sa-east-1.amazonaws.com/images/0FF1D11B-C43B-4D7A-97A3-0357D7896945.jpg",
            "filename": "0FF1D11B-C43B-4D7A-97A3-0357D7896945.png"
        }
    }
}
```
Deverá ser possível manipular os registros através de uma tela e cada vez que o registro for alterado, gerar e armazenar uma versão em JSON do registro.

  

Com os requisitos anteriores cumpridos, proponha um algoritmo que gere um DELTA do registro presente para qualquer versão selecionada do mesmo, permitindo ao usuário escolher o registro e a versão que deseja comparar.

  

O retorno desse algoritmo deverá ser um JSON contendo apenas a diferença entre o registro selecionado e a versão escolhida pela pessoa usuária.

  

Pode ser implementada uma tela para exibir os JSONs, permitindo a quem está utilizando identificar facilmente a diferença entre eles ou gerar o JSON e armazenar em disco.

  
---
Acesso ao S3:
|Chave              |Valor | Observação|
|:--------------------------|:-------------------|:---------|
|Region | sa-east-1|(América do Sul (São Paulo))|
|EndPoint | s3-sa-east-1.amazonaws.com|
|AccesKey | X| Solicitar no momento da implementação |
|SecretKey | X| Solicitar no momento da implementação |
|Raiz do bucket | /teste-dev-delphi/|
--- 


#### Pontos que serão avaliados:
- Lógica;
- Boas práticas de programação;
- Acoplamento e coesão;
- Organização de código;
- Arquitetura proposta;
- Readme para instrução de como fazer o setup do ambiente e rodar o projeto.  

#### Requisitos obrigatórios:
- Requisição HTTPS;
- Armazenamento em banco de dados(relacional ou não relacional);
- Delta de dados (diferença entre versões do registro).

#### Requisitos desejáveis:
- Testes unitários;
- Conexão e download dos arquivos usando S3.

#### **Versão do Delphi recomendada 10.4**
---  

Fique à vontade para propor as telas e a usabilidade da maneira que você quiser.


➡️ Esta etapa é importante para podermos entender qual o seu nível técnico e validar a aderência aos requisitos.

➡️ O resultado do desafio será utilizado exclusivamente para o processo seletivo.

➡️ Para solicitar as credenciais da AWS, envie um e-mail para rafael.muller@nextar.com.br com cópia para matheus.macari@nextar.com.br

➡️ Entendemos que o uso de Inteligências Artificiais é algo corriqueiro e que podem ser grandes aliadas no trabalho, porém, é fundamental que o resultado do desafio entregue por você, reflita quem você é e seus conhecimentos, por tanto solicitamos que caso utilize IAs, que nos envie quais prompts foram utilizados. 

➡️ As únicas pessoas que terão acesso ao seu desafio são a equipe de Delphi e a Recrutadora.

➡️ Todo o nosso processo de recrutamento e seleção está em conformidade com a Lei Geral de Proteção de Dados, a LGPD.

➡️ O prazo de entrega é definido por você a partir da análise do escopo do desafio, por isso, peço que me envie por aqui qual a sua previsão para finalizar o desafio.

➡️ A entrega é feita através do github, compartilhe seu repositorio com os usuarios rafael.muller@nextar.com.br e matheus.macari@nextar.com.br, também envie um e-mail sinalizando a finalização do desafio

➡️ Qualquer dúvida que tiver, não hesite em entrar em contato, estamos sempre à disposição!

Desejamos que seja uma experiência interessante para você desenvolver o Desafio Tech, qualquer dúvida ou se precisar de algum auxílio, estamos à disposição! Desejamos boa sorte!
