# ControlID_AFD_Extractor


A função get_afd() recebe dois parâmetros auth e url com valores padrão de um dicionário que contém informações de autenticação de login e um URL de acesso, respectivamente.

Dentro da função, o módulo requests, json, urllib3 e datetime são importados. A data do dia anterior é calculada usando o método date.today() e timedelta(1) da biblioteca datetime.

A função desabilita os avisos de certificados inválidos usando urllib3.disable_warnings().

Em seguida, a função faz uma solicitação POST usando o método requests.request() com um payload de autenticação e recebe um objeto de resposta. A resposta é transformada em um objeto JSON usando json.loads() e o valor da chave session é atribuído a uma variável session.

A função cria uma URL para obter AFD usando a variável session e a URL de acesso. Um payload é criado com as informações da data do dia anterior.

A função faz uma solicitação POST usando o método requests.request() com um payload de dados do dia anterior e recebe uma resposta. A resposta é escrita em um arquivo de texto com o nome da data do dia anterior e o sufixo _AFD.txt.

Em resumo, a função get_afd() usa as bibliotecas requests, json, urllib3 e datetime para obter um AFD de um sistema de ponto eletrônico, salvar o arquivo de texto com o nome da data do dia anterior e o sufixo _AFD.txt. A função retorna None.
