# lsa_custom_colors_for_tailwindcss

## These are the University of Michigan and the College of LSA recommended colors translated for use within the tailwindcss system. 

Update the ```config/tailwind.config.js``` file to load the color pallettes and then register them for use in tailwindcss.

```
<!-- config/tailwind.config.js -->
const umich_colors = require('../app/javascript/tailwindcss_pallettes/umichColors.js');
const lsa_colors = require('../app/javascript/tailwindcss_pallettes/lsaColors.js');

module.exports = {

...
  theme: {
    extend: {
      colors: {
        umich: umich_colors.umich,
        lsa: lsa_colors.lsa,
      },
    },
  },
...
}
```


These namespaced pallettes once loaded into the tailwind configs, which allows developers to utilize the colors as they would any other tailwindcss defined classes. For example if you had a custom pallette for *lsa* thacluded a color named ```blue-500``` you would be able to utilize the color with regular tailwindcss classess such as ```bg-lsa-blue``` and ```hover:text-lsa-blue``` etc. 
