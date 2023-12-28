# LLM Reward Model

> About

- An LLM response ranking reward model developed using HFRL except the ranking is done by GPT-3.5 instead of humans.
- Essentially ChatGPT is guiding less powerful LLMs to produce better answers (by selecting the best answer from multiple responses).

> Demo

```
System Prompt:
You are a helpful dating coach assistant.



Prompt:
I love a girl, so sweet like an angel. How should I confess my love to her?



Best Response:
It's natural to feel nervous when expressing your feelings to someone, but being true to yourself is the most important thing. Here are some tips on how to confess your love to her:

1. Find the right time and place: It's important to have a quiet, comfortable environment where you can express your thoughts and feelings without any distractions. It's also important to have some alone time with her, so you can both be present and fully focused on the conversation.
2. Be sincere: When expressing your feelings, it's important to be genuine and honest. Don't try to impress her with grand gestures or overly romantic words. Just be true to your feelings and let her know how you feel.
3. Communicate your feelings clearly: Use clear and concise language to express your feelings. Avoid using vague or ambiguous language, and make sure to communicate what it is about her that you love and appreciate.
4. Be prepared for any response: It's important to be prepared for any response she may have. If she's open and receptive, it's a great feeling. However, if she's not ready or not interested, be understanding and respectful.
5. Trust the process: Remember that expressing your feelings is a journey, and it may not always lead to a specific outcome. What's most important is that you're true to yourself and express your feelings honestly.



Second Best Response:
Confessing your love for someone can be one of the most memorable experiences you have with them, it's natural and healthy human connection, but first thing is finding the right way to approach it <|Jap>meiko </>; if they find that sweet they would expect love letters, poems.  A handwritten <|Jap >tangoshizu </Jap or Japanese hand-calligraphy note can go a very long way!  <A note, even
  A short message can say how your feelings for your love interest developed with your special feelings & thoughts
It should be sincere and from the <font color=\"pink\" background=\"#8A8DFE8A8AAB\">bottom </bottom
your  with
and you  it,
You could try to spend some time in private and express why exactly your so attracted with her to
Let her what the feelings mean to you   I wishing for your that to be  good, I  to her



Worst Response:
It's great that you have feelings for someone special! Confessing your love can be nerve-wracking, but it's important to be genuine and honest with yourself and the person you care about. Here are a few tips to help you confess your love to her:

1. Choose a comfortable and private setting: It's important to find a place where you both feel comfortable and relaxed. This could be a quiet spot in a park, a cozy café, or even your own home.
2. Plan ahead: Take some time to think about what you want to say and how you want to say it. Write down a few key points that you want to make, and practice them until you feel confident.
3. Be genuine: When you're ready to confess your love, be genuine and honest with yourself and the person you care about. Don't try to put on a show or say things that you don't truly feel.
4. Be respectful: Remember that the other person may not feel the same way, so it's important to be respectful of their feelings. If they don't feel the same way, try not to take it personally and focus on moving forward.
5. Be patient: Confessing your love can be a big moment, and it's important to be patient and give the other person time to process their feelings. Don't rush the process or push for an immediate response.

Remember, the most important thing is to be true to yourself and the person you care about. Good luck!
```

> Basic Overview

- A 1k dataset of question-response pairs was collected using the OpenOrca dataset and open-source LLMs.
- The responses were ranked from best to worst using GPT-3.5.
- The question-response pairs and ranking were used to train the reward model.
- The reward model can now be applied to any set of responses from LLMs to select the best response.
- This was all done without any human-supervised learning.

> Dataset

- OpenOrca Dataset with 1k responses generated using Mistral-7B-Instruct-v0.1 and Mistral-7B-OpenOrca models.
- Dataset Name: `df_train_first1000_ranked.csv`

> Testing

- Download the Reward Model's .h5 file from the Google Drive link below.
- Run all cells in `Reward_Model_Demo_Module.ipynb` with A100 GPU on Colab.

> Model
 
[Reward Model .h5 Google Drive File Here](https://drive.google.com/file/d/1Tk9RolRS-w31Iw0U-3B7ClOMNdNjSj_R/view?usp=sharing)
