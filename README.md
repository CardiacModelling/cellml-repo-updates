# How to update a model in the CellML repository

_You've downloaded a model, added an annotation or made a bugfix, and now you'd like to share it with the world._

### Step 1: Fork & clone

1. First, it's not called the CellML repository, it's the Physiome (Model) Repository (PMR), and you should be using the URL  https://models.physiomeproject.org.

2. Go to https://models.physiomeproject.org, create an account, and log in

3. Find the model you want to update, e.g. https://models.physiomeproject.org/e/96/grandi_pasqualini_bers_2010.cellml/view
   You are now looking at an _exposure_, a snapshot of a git repository at some fixed point in time.
   ~A bit like~ Exactly like a git tag.
   Exposures are used as a "publication" of a model, frozen at some particular point.

4. Look at the top-right of the page. 
   You should find something saying "Source", and then e.g. _"Derived from workspace Grandi, Pasqualini and Bers, 2010 at changeset 8a2c891da5f2."_
   In other words, you've discovered a link to the git repository!
   (And learned that this exposure has commit hash 8a2c891da5f2).

5. You're now on the "workspace" (repo) page.
   Near the top you should see a toolbar with the options "view", "history", "files", and "fork".

6. Hit "fork" (and fork again) to create your own fork (copy) of this repository.

7. Check "Owner" to see your own name, then "URI for git clone/pull/push" to get a URI to clone

8. Clone the repo onto your system (you will need your account details from step 2)

#### Step 2: Make a change

1. Make some changes

2. Make frequent commits, each with an amazing, informative, time-proof, commit message.

3. Push your changes back up (again using your PMR credentials).

#### Step 3: Bother a curator

1. Get Gary or Michael to email Andre (who's name is David). Or do it yourself.

2. If all goes well, they can
   - pull in your changes to some curated workspace
   - create a new exposure
   - "expire" the old exposure, causing the new one to show up in searches etc. instead



