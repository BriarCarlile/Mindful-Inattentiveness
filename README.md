# Mindful-Inattentiveness
A cloud-based tool for automated storing, tagging, and naming of documents.
In the future, this tool will allow for people to scan their physical documents or existing digital documents and automatically tag and save them.

## Design Concept and Choices
- This application will aim to take 'documents' in via S3 upload, create metadata, and store
- The infrasture is to be a low-cost approach implementing 'features' that can be enabled and disabled
- Each feature will have it's own stack which will allow users to only deploy the features they require
- Key infrastructure stacks, like the control plane stack, are to only create resources for those features being used
- The first 'feature' to be implemented is the use of Textract to evaluate documents, create a searchable clone of the document if needed (scanned) and generate metadata to save alongside the original file
- An uploaded 'document' is to remain unmodified besides the document's name and any object tags that are to be associated with it
