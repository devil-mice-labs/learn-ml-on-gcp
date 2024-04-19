# Machine Learning on Google Cloud

An opinionated collection of resources for getting started with ML on Google Cloud. 

Compiled by your friendly independent consultant [Oliver Frolovs](https://github.com/olliefr) at [`Devil Mice Labs`](https://devilmicelabs.com/) 😈

## Staying up-to-date and exploring possibilities

* [`Data Analytics`](https://cloud.google.com/blog/products/data-analytics) and [`AI & Machine Learning`](https://cloud.google.com/blog/products/ai-machine-learning) sections of [`Google Cloud Blog`](https://cloud.google.com/blog/) feature news, use cases, and best practices. Oddly satisfying.
* [Google Cloud release notes](https://cloud.google.com/release-notes) cover the most recent changes to Google Cloud products and services. This is useful for learning about new features or breaking changes.
* [Google Cloud Architecture Centre](https://cloud.google.com/architecture) offers many end-to-end examples of how Google Cloud services can be connected to solve interesting problems.
* The full list of current [Google Cloud products](https://cloud.google.com/products) with a brief description for each one. Our focus:
  - [AI and Machine Learning](https://cloud.google.com/products#section-3)
  - [Data Analytics](https://cloud.google.com/products#section-7)
  - [Databases](https://cloud.google.com/products#section-8)

For hardcore and very curious techies:

* [GitHub repo with common solutions and tools](https://github.com/GoogleCloudPlatform/professional-services) developed by Google Cloud's Professional Services team. This repository and its contents are not an officially supported Google product. But there are many interesting real-world examples of how Google Cloud services can be used.


## Google Cloud fundamentals

> [!NOTE]
> Regardless of your role, you *should* know about these fundamental services and concepts. The concepts in this section are cross-cutting so they apply in one way or the other to every Google Cloud resource you create or use.

All Google Cloud resources exist in a tree-like [resource hierarchy](https://cloud.google.com/resource-manager/docs/cloud-platform-resource-hierarchy). This hierarchy provides attach points for access control and organisation policies. [`Resource Manager`](https://cloud.google.com/resource-manager) enables you to manage this hierarchy.

<!--
Resource Manager concepts to know: `project`, `folder`, `organisation`.
-->

[`Identity and Access Management (IAM)`](https://cloud.google.com/iam) system lets you grant granular access to specific Google Cloud resources and helps prevent access to other resources. IAM lets you adopt the security principle of least privilege. Read [IAM overview](https://cloud.google.com/iam/docs/overview) to learn how IAM works.

<!--
IAM concepts to know: `Principals`, `Resource`, `Permissions`, `IAM Roles`, `IAM Allow Policy`, `IAM Deny Policy`, `IAM Conditions`
-->

[Using resource hierarchy for access control](https://cloud.google.com/iam/docs/resource-hierarchy-access-control) docs page connects the conceptual models of the two services -- `Resource Manager` and `IAM` to demonstrate how access policies work at different levels of the resource hierarchy and how the policies propagate down the structure of that hierarchy.

[`Cloud Audit Logs`](https://cloud.google.com/logging/docs/audit) – Google Cloud services write audit logs that record administrative activities and accesses within your Google Cloud resources. Audit logs help you answer "who did what, where, and when?" within your Google Cloud resources with the same level of transparency as in on-premises environments.

[Quotas](https://cloud.google.com/docs/quota) restrict how much of a particular shared Google Cloud resource you can use. Learn to [view and manage quotas](https://cloud.google.com/docs/quota_detail/view_manage).

> [!NOTE]
> Many services also have **limits** that are unrelated to the quota system. Limits are fixed constraints, such as maximum file sizes or database schema limitations, which cannot be increased or decreased. You can find out about limits on the relevant Quotas and limits page for your service.

Learn to [create Cloud Billing budgets and alerts](https://cloud.google.com/billing/docs/how-to/budgets) to monitor your spending on Google Cloud.

Learn to [create custom cost controls for BigQuery](https://cloud.google.com/bigquery/docs/custom-quotas) at user and project level.

## Books

* [`Data Science on the Google Cloud Platform` (2nd Edition)](https://learning.oreilly.com/library/view/data-science-on/9781098118945/) is not just for Data Scientists! 

  The book is very hands-on. It shows how to use a variety of Google Cloud services together to solve a problem. You will implement an end-to-end data pipeline –- from ingesting the data to making an operational ML model. 
  
  The book has a [GitHub repo](https://github.com/GoogleCloudPlatform/data-science-on-gcp/) with full source code for many examples. For example, a [machine learning classification model using TensorFlow](https://github.com/GoogleCloudPlatform/data-science-on-gcp/tree/main/10_mlops) with hyperparameter tuning on Vertex AI.

* [`Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow` (3rd Edition)](https://learning.oreilly.com/library/view/hands-on-machine-learning/9781098125967/) explores a range of techniques with numerous code examples and exercises throughout the book help you apply what you've learned. Programming experience is all you need to get started. A useful book to get the "feel" for these popular ML libraries.

## Datasets

The public data sources for your machine learning experiments.

* [UCI Machine Learning Repository](https://archive.ics.uci.edu/)
* [TensorFlow Datasets](https://www.tensorflow.org/datasets)
* [Google BigQuery Open Datasets](https://www.reddit.com/r/bigquery/wiki/datasets/) on Reddit

## Sandboxes

The environments that let you write and execute machine learning (and other) code in your browser.

* [Google Colaboratory]() – zero configuration required, easy sharing, access to VMs and GPUs free of charge.
* ...

## Machine Learning

[Machine Learning Glossary](https://developers.google.com/machine-learning/glossary/) by Google defines many general machine learning terms, plus terms specific to TensorFlow.

Google’s [Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course/ml-intro) is an introduction to (the theory of) machine learning. Ignore the subtitle, there is no need to understand or learn TensorFlow to benefit from this course. All important mathematical concepts are at least referenced here, and many are explained quite well as well.

[Other machine learning courses](https://developers.google.com/machine-learning) by Google are quite interesting too! 😈

[DeepLearning.ai](https://www.deeplearning.ai/courses/) offers a great set of free courses.

[End-to-end user journey for each model on BigQuery ML](https://cloud.google.com/bigquery/docs/e2e-journey) docs page will alert you to what's possible with [`BigQuery ML`](https://cloud.google.com/bigquery/docs/bqml-introduction).

[Generative AI learning path](https://www.cloudskillsboost.google/journeys/118) is one of the great resources available on [Google Cloud Skills Boost](https://www.cloudskillsboost.google/).

## Security

**In addition** to resources listed in the "Google Cloud fundamentals" section:

[`Protecting confidential data in Vertex AI Workbench user-managed notebooks`](https://cloud.google.com/architecture/protecting-confidential-data-in-ai-platform-notebooks) is a blueprint solution by Google to protect your user-managed Vertex AI notebooks.

[`VPC Service Controls`](https://cloud.google.com/vpc-service-controls/docs/overview) can be configured to enforce a security perimeter around your Google Cloud resources, reducing the risk of data exfiltration or data breach.

[`Organisation Policy Service`](https://cloud.google.com/resource-manager/docs/organization-policy/overview) allows you to set *constraints* at various levels of your Google Cloud resource hierarchy, restricting the ways in which these resources can be created and used, thus protecting yourself from security incidents and overspend.

[`Access Transparency`](https://cloud.google.com/assured-workloads/access-transparency/docs/overview) logs are great for keeping an eye on Google personnel accessing your organisation's data 😈 This service is **not** enabled by default, you'd need a paid support package to enable the service. As of the time of writing, the basic support goes for $29 a month which is a steal, IMO, and under the current rules it will qualify you for enabling this service.

## Python

There are too many books, online resources, and courses available on this. I learned a lot from this one -- [`Real Python`](https://realpython.com/). The free version is good but I think the subscription is worth it -- you get access to even more content and they do Office Hours on Slack where there is a very lively learner community.

## Certification

**If you approach it right**, [Google Cloud Certification](https://cloud.google.com/learn/certification) offers a fantastic opportunity both to learn and practice new skills, and to validate your ability to design and build with Google Cloud technology.

> [!WARNING]
> Don't use "exam dumps" or past exams in any shape or form to prepare for your exam. Disregarding the ethical aspect, by skipping study you miss a valuable opportunity to actually learn a useful skill and grow as an individual. Don't do a disservice to yourself.

**Associate** level certification: [Cloud Engineer](https://cloud.google.com/learn/certification/cloud-engineer) 

At the apex of the hierarchy there is **Professional** certification:

* [Cloud Architect](https://cloud.google.com/learn/certification/cloud-architect)
* [Machine Learning Engineer](https://cloud.google.com/learn/certification/machine-learning-engineer)
* [Data Engineer](https://cloud.google.com/learn/certification/data-engineer)
* ... and other roles.

You can (optionally) make your certification record public on [Google Cloud Certified Directory](https://googlecloudcertified.credential.net/profile/f3c409490600bb5cfbdbff2a277d9ef70fbad066?name=frolovs).

For [TensorFlow](https://www.tensorflow.org/) ML library, there is a [TensorFlow Developer Certificate](https://www.tensorflow.org/certificate).

And for infrastructure automation [Terraform Associate](https://www.hashicorp.com/certification/terraform-associate) is the way to go. The official [study guide](https://developer.hashicorp.com/terraform/tutorials/certification-003/associate-study-003) is quite good.

## Notation

The AI products and services sometimes are rebranded and reshuffled. This section keeps a track of notable changes. This is useful because the docs pages and Cloud Skills Boost courses and labs often are updated at a differente cadence so you may see a mix of old and new names.

[`Vertex AI Search and Conversation` is now generally available](https://cloud.google.com/blog/products/ai-machine-learning/vertex-ai-search-and-conversation-is-now-generally-available) (August 29, 2023):

* `Generative AI App Builder` is now `Vertex AI Search and Conversation`, and its components are
  - `Enterprise Search` is now `Vertex AI Search`
  - `Conversational AI` is now `Vertex AI Conversation`
* [`Bard` is now `Gemini`](https://blog.google/products/gemini/bard-gemini-advanced-app/)
* [`Duet AI` is now `Gemini` and `Gemini for Workspace`](https://blog.google/technology/ai/google-gemini-update-sundar-pichai-2024/)
