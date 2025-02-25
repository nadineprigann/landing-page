# Landing Page

This is a very simple and basic landing page I created as an interim solution until the final website is finished and deployed. Therefore, no backend, JS-framework etc. is used. The repo serves as a template to quickly create a basic page and I thought I might as well share this.

##  Preparation

In order to be able to fetch update commits from this template, do not generate a new project from it but rather clone this template and add it as a remote to your project. Here's how to do it:

1. Initialize a (private) repository on GitHub.
2. Run the following commands to duplicate the *landing-page* repository:

```
git clone --bare git@github.com:nadineprigann/landing-page.git
cd landing-page.git
git push --mirror git@github.com:youraccount/project.git
cd ..
rm -rf landing-page.git
```

3. Clone your new repository and add *landing-page* as a remote:

```git remote add default git@github.com:nadineprigann/landing-page.git```

4. Create a dev branch (if not already existing) and publish it to the remote repository.

5. Protect the master branch (see GitHub repository settings).

##  Update repository

Whenever there are new commits made to the *landing-page* that should be applied to one of its instances, simply fetch them:

```git fetch default master```

List the new commits:

```git log --oneline master..default/master```

Pick commits with <a href="https://git-scm.com/docs/git-cherry-pick" target="blank" rel="noopener">git-cherry-pick</a>:

```git cherry-pick -x <commit>```

## Usage

Make sure to update the following parameters to personalize your project. You can use the query ```TEMPLATE``` in your IDE to search for all occurences where you need to update your info. You'll also find a list here:

- **Favicon.** Create one and optimize your favicon via [Real Favicon Generator](https://realfavicongenerator.net/) and extract the contents of the folder into the */favicon* folder.
- **Logo.** Add your logo in SVG format in all 3 *.html* files at the top and update the ```viewBox``` attribute to enable resizing of the SVG. Use [SVGOMG](https://jakearchibald.github.io/svgomg/) for optimization of the file. Review the copyright information within the SVG code to account for proper copyright declaration.
- **index.html.** Adjust, if necessary, your ```<meta>``` of your favicon code (colors, etc.), site title, logo, roles, intro description of what you do and contact information.
- **.VCF file.** Update the desired lines with your information to create a downloadable file that serves as a low key business card. When downloaded, it will be saved to the phone contacts by default.
- **Privacy + Imprint.** Update responsible person, their address, your VAT number, your hoster and the desired form of salutation throughout the text within the docs privacy and imprint. *Please note: currently, these docs are only available in German since it's legally mandatory to have these. If there is demand to translate it to English, I will do so.*
- **CSS.** Search for the location where the CSS variable ```--highlight``` is defined and change the RGB value to your desired highlight color. This is used for the border of the *.vcf* file and the focus style.

If you have any suggestions or changes, please contribute, esp. regarding a11y-updates / -refactors. Happy basic templating!
