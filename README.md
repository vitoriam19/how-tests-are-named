# poc-cc-ufmg-2023-1

Para cada linguagem tem-se:

**1-** Pasta methods_name.
- Contém CSVs com os nomes de métodos extraidos em todos os repositórios da linguagem.
- Contém uma sub pasta com os nomes dos métodos extraídos por repositório, para cada repositório da linguagem.

**2-** Pasta statistics.

Contém 4 arquivos com algumas informações extraídas. Sendo elas:
- prefix_of_each_method: O prefixo de cada método levando em conta todos os repositórios da linguagem.

- quantity_of_characters_per_method: A quantidade de caracteres de cada método extraído de todos os repositórios da linguagem.

- quantity_of_tokens_per_method: A quantidade de tokens, ou seja, de palavras, de cada método levando em conta todos os repositórios da linguagem.

- some_metrics: Fornece algumas métricas númericas interessantes, sendo elas a Quantity of prefix, Quantity total of tokens, Method with the most quantity of tokens, Method with the most quantity of characters, Average number of tokens, and Average number of characters.

**3-** Pasta tokens
- Contém um arquivo chamado tokens.txt com todos os tokens (palavras em cada método) extraídos para todos os métodos de todos os repositórios da linguagem.

- Contém um arquivo chamado tokens_count.txt que consiste num dicionário que mapeia o nome do token (palavra em um método) para a quantidade de vezes que esse token aparece levando em conta todos os métodos de todos os repositórios (ordenado de forma descrecente). Ex: no arquivo tokens_count.txt da linguagem CSharp o token 'Test' aparece 5460 vezes enquanto o token 'Can' aparece 3247 vezes.

- Contém um arquivo chamado tokens_count_lower.txt que faz o mesmo trabalho do arquivo tokens_count.txt, com a diferença de que ele coloca todos os tokens no formato lower case antes de montar o dicionário. Dessa forma, tokens como 'Test' e 'test' que aparecem, respectivamente, 5460 e 2580 vezes no arquivo tokens_count.txt para a  linguagem CSharp, aparece como um único token 'test', no arquivo tokens_count_lower.txt, com valor 8040.

- Contém uma subpasta chamada tokens_info_per_repository, que contém as informações dos tokens separadas por repositório. Dessa forma, para cada repositório, tem-se 6 arquivos que se diferenciam por seu sufixo, sendo eles:
  - *_prefix_of_each_method_result - Uma lista com o prefixo de cada método para o repositório em questão
  - *_quantity_of_characters_result - Uma lista com a quantidade de caracteres de cada método do repositório em questão
  - *_quantity_of_tokens_result - Uma lista com a quantidade de tokens (palavras) de cada método do repositório em questão
  - *_tokens_count - Um dicionário com a chave sendo o token e o valor sendo a quantidade de vezes que aquele token aparece considerando todos os métodos do repositório em questão
  - *_tokens_count_lower - Um dicionário com a chave sendo o token (em lower case) e o valor sendo a quantidade de vezes que aquele token aparece considerando todos os métodos do repositório em questão. Nesse caso, os tokens passam para o formato lower case antes do dicionário ser criado.
  - *_tokens - Uma lista com todos os tokens extraídos de cada método do repositório em questão.

  Além de uma pasta para cada linguagem com as informações acima descritas tem-se também uma pasta de nome pos_tag_info, que contém informações sobre a estrutura gramatical dos tokens analisados para cada linguagem. Essa pasta contém dois arquivos, sendo eles:

  - pos_tag_count: Contém uma lista de tuplas para cada linguagem, mapeando a estrutura gramatical para a quantidade de tokens que se classificam nessa estrutura (levando em conta todos os tokens de todos os métodos de todos os repositórios). Por exemplo: para a linguagem Java, temos uma tupla ('NN', 247812). Essa informação nos diz que para a linguagem Java temos 247812 tokens que são classificados como verbos.

  - pos_tag_count_prefix: Contém uma lista de tuplas para cada linguagem, mapeando a estrutura gramatical para a quantidade de prefixos que se classificam nessa estrutura (levando em conta todos os prefixos de todos os métodos de todos os repositórios). Por exemplo: para a linguagem Java, temos uma tupla ('NN', 72148). Essa informação nos diz que para a linguagem Java temos 72148 prefixos que são classificados como verbos.
