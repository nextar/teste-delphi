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

➡️ Agora que você já sabe o escopo do Desafio, pedimos que nos envie uma previsão de entrega. Em caso de imprevistos ou alterações nas datas, conte conosco que buscamos sempre flexibilizar!

O teste deverá ser entregue através de um repositório no GITHUB, e o link ser enviado para a Jaque, através do e-mail, ou Plataforma Plooral/Geek Hunter, ou WhatsApp (48) 99182-3323.

Desejamos que seja uma experiência interessante para você desenvolver o Desafio Tech, qualquer dúvida ou se precisar de algum auxílio, estamos à disposição! Desejamos boa sorte!
