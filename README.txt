Step 1: We place all the JBake files in src/main/resources directory
Step 2: Then we run the following command to Bake as well as minify the CSS and JS code
        $ mvn jbake:generate;mvn yuicompressor:compress
Step 3: All the output will be generated in the target folder
Step 4: Copy the target folder and place in the NGinX server. We can rename this target folder if we have mentioned another name in the NGinX's config file.
In other words, this target folder is treated as output folder in JBake.

Note: Our original CSS and JS won't be minified, because the above command will generate the output pages
      and minify the CSS and JS only in the target (output) folder.

---------------------------------------------------------------------------

In this project, we have two plug-ins. So, the above command is the combination of the two operations.
One will bake the project and other will minify the CSS and JS code.


