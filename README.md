This is the first scetion of my capstone project focuses on extracting specific information, such as the total price and issue date, from scanned invoices. The primary goal is to demonstrate a comprehensive methodology for everyone who wants to employ a document-oriented multimodal model to identify and extract key information from documents. This process begins with annotation (using free, open-source tools) and concludes in the training of the model.

The project utilized a dataset comprising 141 invoices, which are not for public dataset. To enrich this dataset, 39 invoices from a public dataset (link: https://huggingface.co/datasets/darentang/generated) were also incorporated, bringing the total to 180 invoices. A detailed methodology was then developed, outlining two distinct approaches for addressing the task.

In the absence of pre-existing annotations, the first approach adopted a straightforward solution that bypassed the need for data annotation. This was achieved through Visual Question-Answering (VQA). Here, the user submits an image alongside a question, and the model responds based on its trained knowledge. This exploration of various multimodal document-oriented models for VQA led to the selection of two pre-trained models: layoutlm-invoices(https://huggingface.co/impira/layoutlm-invoices) and LayoutLM-document-QA (https://huggingface.co/impira/layoutlm-document-qa), which were already fine-tuned on datasets bearing similarity to ours.

The second approach, although more labor-intensive, showed greater potential for accurately completing the task. It involved the fine-tuning of LayoutLMv3. Consequently, all 180 documents were annotated by us, resulting in over 600 annotations. By employing LayoutLMv3-base and training it for just a few epochs, we achieved impressive results.

This project outlines a viable pathway for leveraging document-oriented multimodal models to effectively extract key information from a diverse set of documents, starting from the ground up with data annotation and leading to the successful training of such models.

The implementation code is based on the GitHub repository available at: https://github.com/manikanthp/LayoutLMV3_Fine_Tuning
