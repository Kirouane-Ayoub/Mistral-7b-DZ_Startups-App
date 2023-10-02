# Mistral-7b-DZ_Startups App

## Description: 
This project is a web-based chatbot application powered by the Mistral-7b-DZ_Startups model. Users can input text, and the chatbot responds with text-based messages, creating a chat-like interaction.

## Model Information : 
+ **Model Name**: Mistral-7b-DZ_Startups
+ **Model Architecture**: Mistral-7B-Instruct-v0.1
+ **Model Size**: 7.3 billion parameters
+ **Fine-tuned on**: Algerian Startups Dataset V1  by TuningAI Team
+ **https://huggingface.co/ayoubkirouane/Mistral-7b-DZ_Startups**

## Technologies Used
+ **Gradio**: Gradio is used to create the web-based user interface and facilitate real-time communication with the model.
+ **Peft** : Parameter-Efficient Fine-Tuning (PEFT) methods enable efficient adaptation of pre-trained language models (PLMs) to various downstream applications without fine-tuning all the model's parameters.


## Limits : 
+ **Sequence Length**: Due to the use of Sliding Window Attention (SWA), the maximum sequence length may be limited. Ensure that your input data conforms to the model's sequence length restrictions.
+ **Language Support**: The model's primary strength lies in English tasks, but it has been fine-tuned on Algerian Startups data, so its performance in English and code-related tasks may be more reliable.
+ **Fine-tuning Data**: The model's performance is tied to the quality and diversity of the fine-tuning data. Results may vary on tasks unrelated to Algerian startups.


## Ethics considerations : 
+ **Bias Mitigation**: Efforts have been made to reduce bias during fine-tuning, but it's essential to be aware of potential biases in the data and to evaluate model outputs critically.
+ **Fair Use**: Please use this model responsibly and avoid generating content that may be harmful, unethical, or illegal.
+ **Data Privacy**: Be cautious when using sensitive or personal data with this model, as it may inadvertently generate sensitive information.

## Troubleshooting : 

+ If you see the following error:
```
Traceback (most recent call last):
File "", line 1, in
File "/transformers/models/auto/auto_factory.py", line 482, in from_pretrained
config, kwargs = AutoConfig.from_pretrained(
File "/transformers/models/auto/configuration_auto.py", line 1022, in from_pretrained
config_class = CONFIG_MAPPING[config_dict["model_type"]]
File "/transformers/models/auto/configuration_auto.py", line 723, in getitem
raise KeyError(key)
KeyError: 'mistral'
```

**Installing transformers from source should solve the issue:**

```
pip install git+https://github.com/huggingface/transformers
```


## Notice : 

**Mistral 7B** is a pre-trained base model and therefore does not have any moderation mechanisms.

## License
+ **Model License**: Apache 2.0 License

## Getting Started: 

```
pip install -r requirements.txt
python app.py
```
![Screenshot at 2023-10-02 16-46-36](https://github.com/Kirouane-Ayoub/Mistral-7b-DZ_Startups-App/assets/99510125/d6ee3ea2-e8a4-4dd2-8812-202ae2bed5fc)

