We are using the quickstarts repo to document and publish the side-panel help for RHTAP.  
We wanted to have an attribute for the product name (RHTAP) in our side-panel help, to ensure that we remain up-to-date with the changes in the Product Name. I tried something: https://github.com/gtrivedi88/quickstarts/pull/1
But, I'm not sure it would work. It seems the content is populated during database seeding when the pod is uploaded. So when the env variable changes, we would have to spin up new pods. 

Need your help and inputs to solve this situation.
