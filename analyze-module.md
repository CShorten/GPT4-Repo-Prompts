Can you please help me understand the Weaviate module system code?
As a quick primer, Weaviate is a Vector Database that interfaces the ability to search through your data with these modules.
There are many modules in Weaviate such as text2vec, which converts a text query into a vector to use in the database search, (similarly there is img2vec and multi2vec that does the same but with images or a joint image and text embedding space).
Other examples of modules include the qna-transformers that queries a self-hosted question answering app or qna-openai that queries the openai API for question answering.
In both cases of question answering, the module makes some call to the database to access the search functionality.

Can you please explain the design of the generative-openai module?
The file structure is this:
additional
-- generate
---- generate.go
---- generate_graphql_field.go
---- generate_params.go
---- generate_params_extractor.go
---- generate_result.go
---- generate_test.go
-- models
---- models.go
-- provider.go
clients
-- openai.go
-- openai_meta.go
-- openai_meta_test.go
-- openai_test.go
config
-- class_settings.go
-- class_settings_test.go
ent
-- generate_result.go
config.go
module.go

You will receive each file one-by-one and I need you to iteratively build up a summary of the codebase and the purpose of all these files and how they connect to each other.
