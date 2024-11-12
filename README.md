# DITA Topic Model - LinkedIn Topic Model

This repo contains a DITA topic model (TM) related to establishing admin role for a company LinkedIn page.

## Authors

- Lauren Marlier
- Eden Miller
- Brayden Marsh

## Project Maps
- In this section, create subsections for each map, where you will:
  - Write user scenario in your project's README
  - Create an outline for each map that goes along with the user scenario

### User Scenario 1 and Outline
- *note: this user scenario and outline match Lauren's tasks, concept, and reference topics*
- Jane is hired as the new communication specialist for English Inc. As part of her job responsibilites, she must manage all aspects of English Inc.'s company LinkedIn page. In order to do this, her personal LinkedIn account must be designated as a "super admin" in English Inc.'s company LinkedIn page settings but she will need the help a current employee to do this. 
  - .ditamap outline
    - concept: c_what_is_linkedin_admin
    - tasks:
      - t_linkedin_become_company_admin
      - t_linkedin_current_company_admin
    - reference: r_linkedin_roles

### User Scenario 2 and Outline
  *note: this user scenatio and outline match Brayden's task, concept, and reference topics.*
  - John is new to LinkedIn and wants to know what the social media platform is and what types of accounts he can utilize. John wants to learn how to create a LinkedIn account so he can begin to build a network of professionals within his field. 
  #### Ditamap Outline
  - concept: c_what_is_linkedin.dita
  - task: t_linkedin_create_account.dita
  - reference: r_types_of_linkedin_accounts.dita

### User Scenario 3 and Outline
>*Note: This user scenario and outline match Eden's tasks, concept, and reference topics.*
Louise just became social media manager to a student organization. Her club president completed the admin process with her during a club meeting, and now she's ready to start completing her club duties for the account. Since she doesn't have much experience with LinkedIn, she would love to learn more about some basic steps she can take to help monitor the club's account and establish herself as moderator.

#### Ditamap Outline
- concept: c_linkedin_join_request
  - task: t_managing_join_requests.dita
- task: t_writing_a_welcome_post.dita
  - reference: r_linkedin_supported_files.dita

## Folders &amp; Files

- `.github`: Contains configuration files for "Github Actions".
- `assets`: Contains all assets used within the TM.
- `concepts`: Contains all concept topics.
- `references`: Contains all reference topics.
- `tasks`: Contains all task topics.
- `shared`: Contains all topic files that are shared across multiple maps.
- `out`: Contains all output folders.
- `themes`: Contains `.yaml` style configuration files.
- **Skeleton files**: All topic folders contain a single "skeleton" topic file for you to copy, whenever you need to quickly create a new file.
- `.keep` **files**: Ignore these files. They ensure that any empty folders are tracked by git. 
- `.gitignore`: This file tells git which files to ignore in the repo. You can leave this one be.

## Filenaming Conventions

- Task Topics: `t_verb_verbobject.dita`
- Concept Topics: `c_nounphrase.dita`
- Reference Topics: It varies, but something akin to `r_types_of_nounphrase.dita`
- Dita Maps: `_modelname.ditamap`

## Building Outputs with Github Actions

This repo uses Github Actions to create outputs. Refer to the following for details: 

- [.github/workflows/dita-ot-build-actions.yaml](.github/workflows/dita-ot-build-actions.yaml)
- [DITA User Docs - Using Github Actions](https://www.dita-ot.org/dev/topics/using-github-actions)
- [DITA Example YAML files](https://github.com/dita-ot/docs/blob/develop/samples/github-actions/build-using-a-project-file.yaml)

## Building Outputs Manually with the Command Line

See the DITA-OT user guide about how to generate output: [https://www.dita-ot.org/dev/topics/build-using-dita-command](https://www.dita-ot.org/dev/topics/build-using-dita-command)

### Sample DITA Commands

#### Help

To see all of the commands and parameters, use the following command:

```
dita --help
```

#### DITA options and arguments

```
-f == dita output format
-i == dita input map file
-o == dita output directory
-D&lt;property&gt;=&lt;value&gt; == add custom args
    with particular values to dita transformation
-filter &lt;file&gt; == filter and flagging file
```

#### Create an HTML5 site

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```

#### Create an HTML5 site with a custom CSS file

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
  -Dargs.cssroot='url/to/your/assets/folder' \
  -Dargs.css='${cssroot}/your-custom-css-file.css' \
  -Dargs.csspath='css' \
  -Dargs.copycss='yes'
```

#### Create a PDF

```
dita -f pdf -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```
