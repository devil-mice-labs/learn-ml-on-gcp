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


## Must-know Google Cloud concepts

The concepts and services introduced in this section *should* be learned by every Google Cloud practitioner without exception, as they are crucial for access and cost controls and directly or indirectly impact *every action* taken in Google Cloud.

> [!CAUTION]
> A single security incident of the right kind can wipe out your career, if not the entire business you work for. An unexpected cloud bill can turn a profitable year into a year of losses. Don't let it happen to you &mdash; study this section at the earliest opportunity in your cloud journey. 

The remainder of this chapter is split into sections with each section introducing a new core concept or service.

### Resource Hierarchy

You can think of Google Cloud as a collection of services (APIs) such as Kubernetes Engine (API) or Google Cloud Storage (API). You make use of these services (APIs) to provision various **resources** such as Kubernetes clusters and storage buckets. Once a resource is provisioned and configured, you can access and use it.

All those **resources** exist in a tree-like **[resource hierarchy](https://cloud.google.com/resource-manager/docs/cloud-platform-resource-hierarchy)** and you should know about it as well as about its constituent parts such as the `Folder`, the `Project`, and the `Organisation` resources described in the referenced docs page.

The [Resource Manager](https://console.cloud.google.com/cloud-resource-manager), which is a part of IAM section of Google Cloud Console, provides a convenient way to visualise and hierarchically manage resources by project, folder, and organisation. You can find more information about the Resource Manager in its [documentation](https://cloud.google.com/resource-manager/docs).

The resource hierarchy also provides attach points and inheritance for **access management** and **organisation policies**. 

### Identity and Access Management

[`Identity and Access Management (IAM)`](https://cloud.google.com/iam) service lets administrators authorize who can take action on specific resources, giving you full control and visibility to manage Google Cloud resources centrally. Read the [IAM overview](https://cloud.google.com/iam/docs/overview) page to learn how IAM works. The IAM concepts you should know are: `Principals`, `Resource`, `Permissions`, `IAM Roles` (basic and predefined), `IAM Allow Policy`, `IAM Deny Policy`, and `IAM Conditions`.

Now that you know about the **resource hierarchy** and **IAM policies**, read the page that explains how to [use resource hierarchy for access control](https://cloud.google.com/iam/docs/resource-hierarchy-access-control). Remember that the levels of the resource hierarchy &mdash; organisations, folders, and projects provide attach points where the access management policies can be configured.

You should also read [service accounts overview](https://cloud.google.com/iam/docs/service-account-overview).

You might also want to review [IAM best practices](https://cloud.google.com/iam/docs/using-iam-securely).

### Organisation Policies

TODO [Organization Policy Service](https://cloud.google.com/resource-manager/docs/organization-policy/overview)

### Audit Logs

Google Cloud services write audit logs that record administrative activities and accesses within your Google Cloud resources. Audit logs help you answer "who did what, where, and when?" within your Google Cloud resources. You should read [`Cloud Audit Logs overview`](https://cloud.google.com/logging/docs/audit) to learn what kinds of Audit Logs are available and which ones are enabled by default and how this is done. 

Having learned about the different kinds of Audit Logs, you might want to enable some of the optional Audit Logs for your Google Cloud environment. The documentation can tell you what is logged under each kind of Audit Log for different Google Cloud APIs.

Note, that Audit Logs configuration is a part of IAM policy and as such, Audit Logs can be configured at the same levels of Google Cloud resource hierarchy as the IAM policies that were introduced in the previous section. The inheritance also works for Audit Logs configuration.

So hopefully now you can see the connection between the resource hierarchy, the IAM policies, and the Audit Logs configuration.

TODO [Access Transparency](https://cloud.google.com/assured-workloads/access-transparency/docs/overview)

### Quotas and Limits

[Quotas](https://cloud.google.com/docs/quota) restrict how much of a particular shared Google Cloud resource you can use. Learn to [view and manage quotas](https://cloud.google.com/docs/quota_detail/view_manage).

Many services also have **limits** that are unrelated to the quota system. Limits are fixed constraints, such as maximum file sizes or database schema limitations, which cannot be increased or decreased.

### Billing budgets and exports

Learn to [create Cloud Billing budgets and alerts](https://cloud.google.com/billing/docs/how-to/budgets) to monitor your spending on Google Cloud.

### BigQuery

Learn to [create custom cost controls for BigQuery](https://cloud.google.com/bigquery/docs/custom-quotas) at user and project level.

## Books

* [`Data Science on the Google Cloud Platform` (2nd Edition)](https://learning.oreilly.com/library/view/data-science-on/9781098118945/) is not just for Data Scientists! 

  The book is very hands-on. It shows how to use a variety of Google Cloud services together to solve a problem. You will implement an end-to-end data pipeline –- from ingesting the data to making an operational ML model. 
  
  The book has a [GitHub repo](https://github.com/GoogleCloudPlatform/data-science-on-gcp/) with full source code for many examples. For example, a [machine learning classification model using TensorFlow](https://github.com/GoogleCloudPlatform/data-science-on-gcp/tree/main/10_mlops) with hyperparameter tuning on Vertex AI.

* [`Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow` (3rd Edition)](https://learning.oreilly.com/library/view/hands-on-machine-learning/9781098125967/) explores a range of techniques with numerous code examples and exercises throughout the book help you apply what you've learned. Programming experience is all you need to get started. A useful book to get the "feel" for these popular ML libraries.

* Stuart Russell and Peter Norvig’s `Artificial Intelligence: A Modern Approach, 4th edition (Pearson)`, is a great (and huge) book covering an incredible amount of topics, including machine learning. It helps put ML into perspective.

## Code samples

Samples showcasing Google Cloud for machine learning and data applications.

### [Google Cloud · Generative AI](https://github.com/GoogleCloudPlatform/generative-ai)

`github.com / GoogleCloudPlatform / generative-ai`

Sample code and notebooks for Generative AI on Google Cloud, with Gemini on Vertex AI.


### [Google Cloud Applied AI Engineering team · Samples](https://github.com/GoogleCloudPlatform/applied-ai-engineering-samples)

`github.com / GoogleCloudPlatform / applied-ai-engineering-samples`

This repository contains code samples and notebooks demonstrating how to use Generative AI on Google Cloud Vertex AI.

### [Advanced Solutions Lab · ML Immersion](https://github.com/GoogleCloudPlatform/asl-ml-immersion)

`github.com / GoogleCloudPlatform / asl-ml-immersion`

This repository contains Jupyter notebooks meant to be run on Vertex AI. It is maintained by Google Cloud's [Advanced Solutions Lab (ASL)](https://cloud.google.com/asl) team.

In particular, the notebooks in this repository cover a wide range of model architectures targeting different data modalities implemented mainly in Tensorflow and Keras, as well as the tools on Google Cloud's Vertex AI for operationalizing Tensorflow, Scikit-learn and PyTorch models at scale (e.g. Vertex training, tuning, and serving, TFX and Kubeflow pipelines).


### [Google Cloud · Vertex AI Samples](https://github.com/GoogleCloudPlatform/vertex-ai-samples)

`github.com / GoogleCloudPlatform / vertex-ai-samples`

This repository contains notebooks, code samples, sample apps, and other resources that demonstrate how to use, develop and manage machine learning and generative AI workflows using Google Cloud Vertex AI.


### [Cloud Learning Services · Specialized Training Resources](https://github.com/GoogleCloudPlatform/specialized-training-content)

`github.com / GoogleCloudPlatform / specialized-training-content`

This repository contains files that are used for instructor-led training courses as part of the Cloud Learning Services Specialized Training program. These files are used in classroom demos, hands-on lab activities, and for supplemental discussions around course topics. Files are organized by course.


### [Google Cloud Training · Data Analyst](https://github.com/GoogleCloudPlatform/training-data-analyst)

`github.com / GoogleCloudPlatform / training-data-analyst`

Labs and demos for courses for [GCP Training](http://cloud.google.com/training).


### [Google Cloud Platform · Python Samples](https://github.com/GoogleCloudPlatform/python-docs-samples)

`github.com / GoogleCloudPlatform / python-docs-samples`

Python samples for [Google Cloud Platform products](https://cloud.google.com/).


<!--
### [WHO · WHAT](HTTPS)

`github.com / GoogleCloudPlatform / REPO`

DESCRIPTION
-->

## Datasets

The public data sources for your machine learning experiments.

* [UCI Machine Learning Repository](https://archive.ics.uci.edu/)
* [TensorFlow Datasets](https://www.tensorflow.org/datasets)
* [Google BigQuery Open Datasets](https://www.reddit.com/r/bigquery/wiki/datasets/) on Reddit
* [Hugging Face](https://huggingface.co/)

## Sandboxes

Environments for writing and running code in your browser.

### [Google Colaboratory](https://colab.google/)

[Open Colab](https://colab.research.google.com/) · [New Notebook](https://colab.new/)

Colab is a hosted Jupyter Notebook service that requires no setup to use and provides free access to computing resources, including GPUs and TPUs. Colab is especially well suited to machine learning, data science, and education.

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

You can opt in to have your earnder certification credentials public on [Google Cloud Skills Directory](https://www.credly.com/organizations/google-cloud/directory), powered by Credly.

For [TensorFlow](https://www.tensorflow.org/) ML library, there is a [TensorFlow Developer Certificate](https://www.tensorflow.org/certificate).

And for infrastructure automation [Terraform Associate](https://www.hashicorp.com/certification/terraform-associate) is the way to go. The official [study guide](https://developer.hashicorp.com/terraform/tutorials/certification-003/associate-study-003) is quite good.

## Renamed products

*Some* changes in product names. You might see the old names in some places—for example, in videos.

* *Vertex AI Search and Conversation* is now *Vertex AI Agent Builder* [:link:](https://cloud.google.com/generative-ai-app-builder/docs/release-notes#April_24_2024) (April 24, 2024)
  - `Vertex AI Search` kept its name
  - `Vertex AI Conversation` to `Vertex AI Agents`
* *Generative AI App Builder* is now *Vertex AI Search and Conversation* [:link:](https://cloud.google.com/generative-ai-app-builder/docs/release-notes#October_09_2023) (October 09, 2023)
  - `Enterprise Search` to `Vertex AI Search`
  - `Conversational AI` to `Vertex AI Conversation`

* [`Bard` is now `Gemini`](https://blog.google/products/gemini/bard-gemini-advanced-app/)
* [`Duet AI` is now `Gemini` and `Gemini for Workspace`](https://blog.google/technology/ai/google-gemini-update-sundar-pichai-2024/)

* `Vertex AI` was `AI Platform` until [:link:](https://cloud.google.com/vertex-ai/docs/release-notes#May_18_2021) May 18, 2021. Some APIs and endpoint domain names still use the old name.
