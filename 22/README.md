# Human perception of screen brightness

Recently I read this article about ["Changing screen brightness in accordance with human perception"](https://konradstrack.ninja/blog/changing-screen-brightness-in-accordance-with-human-perception/). 
This article mainly talks about, how the difference between **90%** and **95%** of brightness is significantly less than the difference between **5%** to **10%**.
It is because how our eyes and brain works.

According to the **The Weber-Fechner Law**, perceived brightness is more or less proportonial to the logarithm with base 10. 
Which is why, there is only so little a difference between **90%-95%** of brightness, because `log(90)` and `log(95)` is not that far apart from each other. That is not the case for `log(5)` and `log(10)`.

Using [brillo](https://github.com/cameronnemo/brillo), we can control screen brightness logarithmically from the terminal. [This script](https://raw.githubusercontent.com/ericmurphyxyz/dotfiles/master/.local/bin/changebrightness) leverage this software to control brightness and sends notifications to let the use know about their current brightness level.
