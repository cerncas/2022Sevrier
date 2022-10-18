
## Notes for the maintainer and presenter

###  Known schools using this material

- [CAS 2019 in Slangerup](https://indico.cern.ch/event/780638/)


### Edit the material

The material is hosted on github under the [cerncas organisation](https://github.com/cerncas/) and mirrored (for backup purposes) to the CERN GitLab [CAS group](https://gitlab.cern.ch/cas).
One is expected to edit the material:

1. from **github directly** using the github editor
2. from **one's computer** cloning the repository, editing/adding/deleting the desired content, finally pushing the content to github

### (CERN) GitLab vs GitHub

See article [KB0003132](https://cern.service-now.com/service-portal?id=kb_article&n=KB0003132) to learn about CERN policy.
To setup a "Pull mirroring" on the CERN GitLab to retrieve a copy of GitHub repository, see the [official documentation](https://docs.gitlab.com/ee/user/project/repository/mirror/pull.html).

### Create a pdf of an .md file

The typically suggested way is to use `pandoc` package:

```bash
pandoc Setup_Instructions.md -o Setup_Instructions.pdf
```

unfortunately, this doesn't work when you have HTML inside your `.md` file, as we presently have...
A solution could be to use the [Print extension](https://marketplace.visualstudio.com/items?itemName=pdconsec.vscode-print) for VisualStudio...

### During the course

The students are expected to download [Exercises.ipynb](./Exercises.ipynb) on their computer, and open it using Jupyter Lab.
The presenter can also use Jupyter Lab and do the exercise with the students. To launch Jupyter Lab, move in a terminal to this folder and execute:

```bash
jupyter lab
```

One can also present [Exercises_Solutions.ipynb](./Exercises_Solutions.ipynb) in presentation mode:

```bash
jupyter nbconvert Exercises_Solutions.ipynb --to slides --post serve
```

Alternatively, one can:

- create a **html** of the slides:
   ```bash
   jupyter nbconvert Exercises_Solutions.ipynb --to slides
   ```
- create a **pdf** of the slides:
   ```bash
   conda install pandoc
   jupyter nbconvert Exercises_Solutions.ipynb --to pdf
   ```