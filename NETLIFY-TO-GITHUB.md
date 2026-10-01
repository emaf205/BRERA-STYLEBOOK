# One-time Netlify → GitHub setup

This package is designed for the existing Netlify project:

`https://brera-stylebook.netlify.app/`

## First time

1. Drag this site folder into Netlify Drop / deploy it to the existing project.
2. Verify the live site.
3. In Netlify open **Project configuration → Build & deploy → Continuous deployment → Repository**.
4. Choose **Push to new repository**.
5. Create the public GitHub repository, preferably `BRERA-STYLEBOOK`.

Netlify pushes the deployed project files into the new repository.

## After the repository exists

The source of truth changes direction:

**GitHub → Netlify**

Future commits pushed to the connected GitHub repository trigger Netlify deploys automatically. Do not keep using manual Drop deploys for normal updates once continuous deployment is connected.
