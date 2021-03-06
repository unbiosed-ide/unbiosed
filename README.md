# unBIOSed IDE
___THIS PROJECT IS NOT ACTIVE ANYMORE___
___I'm not working with UEFI development anymore so I can't keep up with new developments on EDK. Feel free to fork this repo and let me know so that I can link to a version that's actively maintained here.___

This project is an Eclipse environment that aims to provide a set of features on top of Eclipse CDT to ease the development of EDK2-based UEFI modules.

This is a work in progress, so feel free to suggest new features and let me know if you find any bugs while using it :)

# A tour

[![unBIOSed](http://img.youtube.com/vi/BgUr8osUEhg/0.jpg)](https://www.youtube.com/watch?v=BgUr8osUEhg)

# Build instructions
  Clone this project with the command `git clone --recursive https://github.com/unbiosed-ide/unbiosed.git` and run `mvn verify`. This will generate the plugin's update size as a ZIP file under `releng/me.fmartins.unbiosed.update/target`.
  
# Plugin installation in Eclipse CDT Mars
 Add the update site generated by the build as a local update site to your Eclipse CDT instance. This can be done by clicking in **Help** --> **Install new software** --> **Add** button --> **Archive** button and then selecting the ZIP file that contains the plugin update site. After that, select the new update site, check the **unBIOSed Tools** box and follow the dialog pages to install the plugin.
 After restarting Eclipse, the plugin features will become available in the IDE.
 
# Known issues
   - Sometimes, the source indexer doesn't immediately gets everything right for large projects(which means that autocomplete and syntax highlighting won't work, for instance). A quick fix around it is to rebuild the index by right-clicking the project and selecting *Index* --> *Rebuild*;

# Current status
  - Existing EDK2 Module project wizard:
    - ~~Import .inf file;~~
    - ~~Populate project sources in Project Explorer view;~~
    - ~~Add include paths extracted from the .dec files referenced in the module's .inf file;~~
    - ~~Add custom workspace path to the project wizard;~~
    - Add build steps to the new project;
  - New EDK2 Module project wizard:
    - Initial setup page(Module name, module type, referenced packages(.dec), consumed library classes, protocols and GUIDs);
    - Platforms page(which .dsc files will included the new module);
    - New library class implementation page;
    - UEFI Driver settings page(driver type, depex, etc);
