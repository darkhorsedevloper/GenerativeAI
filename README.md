# GenerativeAI 
Working with AWS Bedrock and Generative AI ( FMs ) 

*This project was done in conjunction with ZTM to learn how to work with AWS Bedrock and all of the features offered with foundational models.  I am not fine-tuning models with my data but I am looking forward to learning.* 

## What is Amazon Bedrock?

AWS Bedrock was created by Amazon to streamline the process of using powerful AI models across a range of use cases. It offers a broad set of capabilities to support the development and scaling of generative AI applications.
Plus, it helps developers easily build generative AI applications with enhanced security, privacy, and responsible AI practices. 
It is a fully managed service that provides access to a variety of high-performing foundation models (FMs) from leading AI companies such as *A121 Labs, Anthropic, Cohere, Meta, Mistral AI, Stability AI, and Amazon,* all through a single API.
AWS Bedrock allows you to interface with other innovative companies' models and allows you to choose the right model for your use case and customize models with your data. 
A huge benefit is that with AWS, data adheres to privacy and security policies, such as having HIPPA eligibility and adhering to GDPR compliance.

##  What are foundational models?

A term coined by researchers to describe models trained on a broad spectrum of unlabeled data and capable of performing a wide variety of tasks, such as generating text and images, conversing in natural language, and understanding language. Foundational Models are poised to significantly change the machine learning life cycle. It is faster to use these to create new applications and cheaper, as training models from scratch is very expensive. Models are trained on massive data sets and large deep-learning neural networks. *Foundation models are a starting point.*  They are great for creating applications such as customer support, copywriting, automating tasks and processes, language translation, high-resolution image creation, robotics, healthcare, and autonomous vehicles. They are a form of generative AI as they generate output from one or more inputs or prompts in the form of human language instructions. They are based on complex neural networks including generative adversarial networks, GANS, transformers, and variational encoders. Although each type of network functions differently, the principles behind how they work are similar. In general, a foundational model uses learned patterns in relationship to predict the next item in a sequence. For example, with image generation, the model analyzes the image and creates a sharper more clearly defined image. Similarly, with text, the model predicts the next word in a string of text from the previous words and its context and then selects the next word using probability distribution techniques. They use self-supervised learning to create labels from input data. This means that no one has instructed or trained the model with labeled training data sets. This feature separates LLMs from previous machine learning architecture which supervised or unsupervised learning. Models here in Bedrock or ChatGPT are better than an old-school algorithm because traditional models create a single static vector for each word, while models like Elmo, Bert, and GPT generate dynamic embeddings based on the context in which word appears and this allows them to capture more neurons meanings and the ability to handle poly-semi, words that can have more than one meaning in context. It also offers Retrieval Augmented Data ( RAG ), vector databases, word embeddings, serverless AI applications, training, and evaluation of LLMs with your custom data. - summarized from ZTM

### Inference Configuration for LLMs and Image Generative Models

*Closer to 0,( higher prob)  further away from 0 ( lower prob )*

 - **Temperature -** -  LLMs use probability to construct the words in a sequence. For any given sequence there is a probability distribution of options for the next word in the sequence. The temperature modulates the probability density function for
 the next tokens. This parameter can deepen or flatten the density function curve. A lower value results in a steeper curve with more deterministic responses and a higher value results in a flatter curve with more random responses. 
- **Top K -** defines the cut-off where the model no longer selects the words. Lower reduces the probability that an unusual word gets selected next in a sequence. The number of highest probability vocabulary tokens to keep for top k filtering.
- **Top P -** defines a cut-off based on the sum of probabilities of the potential choices. Setting it below one the model considers the most probable options and ignores less probable ones. It caps choices based on the sum of their probability.
- **Length -** maximum number of tokens to generate - especially comes in handy if you want to look at this from a pricing perspective.
- **Stop-Sequences -** Configure up to 4 sequences that the model recognizes where the API will stop generating further tokens. The returned text will not contain the stop sequence.
- **Return Likelihoods-** All or None - specifies how and if the token likelihoods are returned with the response. The default option is None.
- **Streaming -** how you would like your response returned. Piece by Piece or after the response is finished using true or false.
- **Seed -**  Determines the initial noise setting. If you use the same seed as a previous run to allow inference to a previous generation.

### Fine-tuning and Training models with your custom data

- **Embedding model -** Embedding models create a vector output and this means that you can have text and it will save it as an embedding and you can use the embedding to save your data into a vector database and you can do semantic searches, etc. It only outputs a vector with the size specified.
- **Custom Models -** train and fine-tune with your custom data. Data is encrypted by default with an AWS-owned key but you can also choose your own key. Use input and validation set from an s3 bucket. You can adjust hyper-parameters ( epochs, batch size, learning rate, and learning rate warmup sets ). You will store output data in an s3 bucket. You are required to use provisioned throughput.





 
