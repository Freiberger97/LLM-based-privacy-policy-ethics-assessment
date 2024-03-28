# LLM-based-privacy-policy-ethics-assessment
We systematically prompt GPT 3.5 turbo to investigate the ethics of privacy policies. This repository contains the prompts we utilized to conduct 9240 experiments over 55 policies. 

**Prompts:**

The folder "prompts" structures our prompt variations as follows:

    "prompts" contains the original German prompts.
    "prompts_en" contains the English translations of the prompts.
    "prompts_para" contains the paraphrased German prompts
    It also contains the user prompt template in English and German.

All folders regarding prompts are structured in the following way: 

"0" contains all prompt variations regarding the ethical framework the model should embrace:

    0.txt assigns Consequentialism as a baseline to argue. Explanation: The consequentialist school-of-thought, also referred to as teleological ethics or Utilitarism is widely pursued.
    1.txt assigns Deontology as a baseline to argue. Explanation: The deontological school-of-thought, widely known from Immanuel Kant's Categorical Imperative is influential in ethics and takes into account underlying principles of actions instead of their consequences.
    2.txt assigns Virtue ethics as a baseline to argue. Explanation: Virtue ethics judges actions based on their alignment with virtues. Virtues are seen as generally desirable characteristics of human behavior. It is seen as a major approach to ethics. This offers a distinct perspective for assessing ethics.
    2.txt assigns no such established framework to argue with. Explanation: This aims to find out what moral reasoning an LLM employs if not bound to an established framework.

"1" contains all prompt variations assigning roles to the LLM from which it should pursue the assessment:

    0.txt assigns the role of an independent ethicist. Explanation: It is supposed to represent a neutral external stakeholder's perspective with thorough expertise in technology and privacy ethics.
    1.txt assigns the role of a politician. Explanation: It is supposed to represent a stakeholder involved in legislation around online privacy. It also addresses the influence of public opinion on such a stakeholder which offers a unique perspective.
    2.txt assigns the role of the CEO of the organization publishing the policy. Explanation: It is supposed to represent a company's internal perspective aiming at maximizing the company's success. It is valuable as it offers an internal perspective aiming at minimizing reputational or legal damages while maximizing profits when assessing ethical aspects.
    3.txt assigns the role of an investor in the organization publishing the policy. Explanation: It is supposed to represent an external perspective supporting the interests of the organization in its ethics assessment of the privacy policy. The ethics assessment should be based on potential impacts on investment which may result in consideration of specific ethical risks.
    4.txt assigns the role of an average user of the application. Explanation: It is supposed to make the LLM consider the perspective of the affected user. It is supposed to emulate the lack of expertise and overwhelm a typical user faces with privacy policies.
    5.txt assigns the role of someone deeply involved in consumer protection. Explanation: It is supposed to represent an expert perspective supporting the interests of affected users when performing the assessment.
    6.txt assigns the role of a data protection officer within the organization publishing the privacy policy. Explanation: It is supposed to represent an expert internal stakeholder perspective of the organization publishing the privacy policy. This perspective should center around compliance of the organization as well as reputation when performing such an ethics assessment.

"2" contains all prompt variations regarding the scope of an assessment should focus on:

    0.txt sets a local scope of the assessment. Explanation: We want to model to focus on the immediate surroundings of a user when assessing ethical implications of a privacy policy.
    1.txt sets a global scope of the assessment. Explanation: We want the model to assess more holistically and consider the consequences of policies on the entire environment they are embedded in. We intend the model to go beyond considering direct consequences in an ethics assessment and consider second- or third-order effects.
    3.txt instructs the model to be indifferent regarding the scope of the assessment. Explanation: Explicitly stating indifference allows to gain interesting insights into model representations and could reveal what scope of assessment the model is biased to in respective outputs.

"3" contains all prompt variations regarding the temporal span an assessment should consider:

    0.txt sets a short-term focus for the assessment. Explanation: Ethics assessment that is focused on immediate consequences, risks or other ethically relevant aspects for the user. Should complement the other time spans for assessment. 
    1.txt sets a mid-term focus for the assessment. Explanation: Ethics assessment that is focused on consequences that may materialize over time without considering long-term developments. Should complement the other time spans for assessment.
    2.txt sets a long-term focus for the assessment. Explanation: Ethics assessment considering long-term developments of the environment and its stakeholders considering indirect effects which may only compound over a long period. Should complement the other time spans for assessment.
    3.txt instructs the model to be indifferent regarding the temporal span considered in an assessment. Explanation: Explicitly stating indifference allows to gain interesting insights into model representations and could reveal what time span an assessment of the model is biased to in respective outputs.

"4" contains all prompt variations regarding the user interests the model should consider:

    0.txt assumes users to be mainly interested in the trustworthiness of the privacy standards established in the privacy policy. Explanation: Different users may have quite different interests. Trustworthiness provides an umbrella term that captures a few different aspects that are perceived as relevant and it is deeply embedded in ethics.
    1.txt assumes users to be mainly interested in the fairness of the privacy standards established in the privacy policy. Explanation: Fairness is a concept which is deeply related to ethics and should be considered in an assessment as it is relevant, particularly to marginalized user groups.
    2.txt assumes users to be mainly interested in the morality of the privacy standards established in the privacy policy. Explanation: We wanted to include a broader framing of user interests with morality to gain insight into what an LLM focuses on given such a broad concept.
    3.txt assumes users to be mainly interested in minimizing risks exposure from the privacy standards established in the privacy policy. Explanation: Risk and vulnerabilities are a focus of the fair balancing aimed at by the GDPR. It captures a baseline to argue on when assessing ethics and is certainly relevant to users.
    4.txt assumes users to be mainly interested in the general societal good and how that is captured in the privacy standards established in the privacy policy. Explanation: This variation tries to represent an altruistic perspective some users may have. It is more holistic and optimizes for society instead of the individual.
    5.txt assumes users to be mainly interested in accountability mechanisms established in the privacy policy. Explanation: Accountability mechanisms are important to users as they ensure the integrity and compliance with privacy standards established in a policy. It offers a relevant perspective when assessing ethics.
    6.txt assumes users to be mainly interested in ethical data use. Explanation: We include a broader framing of user interests with data ethics to gain insight into what an LLM focuses on given such a broad concept.
    7.txt assumes unknown user interests. Explanation: We want to find out what the LLM bases its assessment on if no user interests are known. This gives insight into the representations present in the model.
    8.txt assumes the interests of an average user. Explanation: We want to find out what the LLM identifies as average user interests and what it deems relevant for ethics assessment based on that. This gives insight into the representations present in the model.

"baseline.txt" contains the baseline prompt without variations.

**Outputs:**

All outputs are contained in the file named "Ethics_Assessment_outputs.zip".

**Privacy** **Policies:**

The original policy texts of the 55 privacy policies we assessed are in the folder named "Policy_Texts"
