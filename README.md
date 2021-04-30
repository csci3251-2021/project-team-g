# Introduction ⭐
We are going to build a [web page](https://csci3251-2021.github.io/project-team-g/) step by step.
A project board is created so that everyone can keep track of progress.
1. Everyone will include his or her profile in the `_stu` folder, which will be displayed under **Contributors**. 
2. A Github Action with a workflow will be set up to run the C code written in `code.c`, from which a status badge will be obtained and be displayed under **Code**.
3. The last updated time of the repo will be included at the bottom of the web page.
4. Finally, the link of our webpage will be added to the `README.md` in `csci3251-2021.github.io` in the CSCI3251-2021 organization.

# Code 💻
 ```c
 {% include_relative code.c %}
 ```
 ![](https://github.com/csci3251-2021/project-team-g/actions/workflows/c-cpp.yml/badge.svg)
 
 # Contributors 🧑‍🤝‍🧑
{% for stu in site.stu %}
  * <img src="{{ stu.image }}" style="width: 40px; height: 40px"> [@{{stu.user}}](http://github.com/{{stu.user}}) ({{stu.name}}) 
    * {{ stu.content }}
{% endfor %}

{{ site.time }}
