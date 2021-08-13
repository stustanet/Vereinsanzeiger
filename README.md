# Vereinsanzeiger des StuStaNet e. V.

## Add a new page

After cloning this project, you first need to install hugo.
```shell
# On debian based systems
sudo apt install hugo
# On arch
sudo pacman -S hugo
```

Then go into the project folder and run the `hugo new` command:
```shell
cd vereinsanzeiger
hugo new history/<page_name>.md
```
Now open this file e.g. `vim content/history/<page_name>.md`.
Note, the meta data that has been created in the beginning of the document separated by `---`.
Edit the `title`, this will be displayed as the posts title. You can leave `date` unchanged. This will determine the data displayed in the top right of the post.
`draft` should also be left unchanged, if set to false the post will not be included in the rendered webpage. `display_on_front_page` determines weather the post
should be displayed on the index page. Since we `history` lists all old posts it makes sense to have this flag only set to true for the latest 1-3 posts.


The rest of the file is the content and it can be written in normal markdown syntax. The project includes a hugo shortcode to use bootstrap formatted tables. 
For an example see `content/history/haw_ss21.md`.

## Advanced
To change the layout of the front page see `layouts/index.html` and the base layout file in `layouts/_defaults/baseof.html`.
In order to edit single posts pages (yes they exist under history/<post_file_name_without_md>) see `layouts/_defaults/single.html`. For the listing in history see `layouts/_defaults/list.html`.
CSS and PDFs are in `static`.