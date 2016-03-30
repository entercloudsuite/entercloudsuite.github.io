# Enter Cloud Suite Guides
<http://entercloudsuite.github.io>

&nbsp;

#### How to edit this website

1. **LOCAL DEVELOPMENT**
    * Download the [Github Desktop Client](https://desktop.github.com/) and sync the repo
    * Install [Jekyll](https://jekyllrb.com/)
    * Edit the files and push to Github when finished

&nbsp;

#### Creating a new post

1. Open the posts folder

2. Create a new file named **YYYY-MM-DD-title-of-the-post.markdown**

3. Insert the front matter:
   * **layout:** define the page layout. Default value is "post".
   * **title:** the title of the post. Make it SEO friendly and put it into quotation marks: "Example Post"
   * **date**: the creation date. The format should be: YYYY-MM-DD HH:MM:SS
   * **last_modified_at**: last edited date. The format should be: YYYY-MM-DD HH:MM:SS
   * **excerpt**: the summary of the post. Make it SEO friendly and put it into quotation marks: "Description"
   * **categories**: category-name (it could be: computing, support, logs, object-storage, networks, cdn, dns-domains, projects, tags, add-ons, reports, admin-portal)
   * **tags**: tag-name (optional)
   * **image**:
      * **feature**: image.jpg (put one file in the folder assets/images/hero resolution 2000x1000px and one file with the same name in the folder assets/images/thumbnail resolution 800x400px - if you need help ask Francesca)
      * **topPosition**: 0px
   * **bgContrast**: dark
   * **bgGradientOpacity**: lighter
   * **syntaxHighlighter**: yes (if there's code inside the text it loads the javascripts for highlighting)
   
4. Edit the post content with Markdown. For a Syntax reference, see <http://kramdown.gettalong.org/quickref.html>

5. If the post has images, put them into the folder assets/images/posts

6. For additional examples, custom styles and more check the **example-post.md** file in the **_drafts** folder.
