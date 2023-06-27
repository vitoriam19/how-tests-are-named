# File structure and content

For each language we have:

**1-** methods_name folder

- Contains CSVs with method names extracted from all language repositories.
- Contains a subfolder with the names of methods extracted by repository, for each language repository.

**2-** statistics folder

Contains 4 files with some extracted information. Being them:
- prefix_of_each_method: The prefix of each method taking into account all language repositories.

- quantity_of_characters_per_method: The amount of characters of each method extracted from all language repositories.

- quantity_of_tokens_per_method: The quantity of tokens, that is, words, of each method taking into account all language repositories.

- some_metrics: Provides some interesting numerical metrics, such as "Total quantity of prefixes", "Total quantity of tokens", "Method with the most quantity of tokens", "Method with the most quantity of characters", "Average number of tokens", and "Average number of characters".

**3-** tokens folder

- Contains a file called `tokens.json` with all tokens (words in each method) extracted for all methods from all language repositories.

- Contains a file called `tokens_count.json` which consists of a dictionary that maps the token name (word in a method) to the number of times that token appears taking into account all methods from all repositories (ordered in descending order). For example: in the C# file `tokens_count.json`, the 'Test' token appears 5460 times while the 'Can' token appears 3247 times.

- Contains a file called `tokens_count_lower.json` that does the same job as the file `tokens_count.json`, with the difference that it places all tokens in lower case format before building the dictionary. Thus, tokens like 'Test' and 'test' that appear, respectively, 5460 and 2580 times in the `tokens_count.json` file for the C# language, appear as a single 'test' token, in the `tokens_count_lower.json` file, with a value of 8040.

- Contains a subfolder called `tokens_info_per_repository`, which contains token information separated by repository. Thus, for each repository, there are 6 files that differ by their suffix, namely:

  * *_prefix_of_each_method_result - A list with the prefix of each method for the given repository.
  * *_quantity_of_characters_result - A list with the amount of characters of each method of the given repository.
  * *_quantity_of_tokens_result - A list with the amount of tokens (words) of each method of the given repository.
  * *_tokens_count - A dictionary with the key being the token and the value being the number of times that token appears considering all methods of the given repository.
  * *_tokens_count_lower - A dictionary with the key being the token (in lower case) and the value being the number of times that token appears considering all methods of the given repository. In this case, the tokens are in lower case format before the dictionary is created.
  * *_tokens - A list of all tokens extracted from each method in the given repository.

**4-** POS tag folder

In addition to a folder for each language with the information described above, there is also a folder named pos_tag_info, which contains information about the grammatical structure of the analyzed tokens for each language. This folder contains one file, namely:

- pos_tag_count_prefix: Contains a list of tuples for each language, mapping the grammatical structure to the number of prefixes classified in this structure (taking into account all prefixes of all methods of all repositories). For example: for the Java language, we have a tuple ('NN', 134422). This information tells us that for the Java language we have 134422 prefixes that are classified as nouns.
