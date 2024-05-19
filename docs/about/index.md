---
hide:
  - navigation
  - feedback
  - toc
search:
  exclude: true
icon: material/account-box
---

# I'm Rahul Kumar

<style>
  @media (min-width: 900px) {
    main > div > div.md-content {
      max-width: 75%;
      margin: auto;
    }
  }
  article > h1 { display: none; }
</style>

<p style="text-align: center; margin: 0px;" markdown>
  <img src="https://avatars.githubusercontent.com/u/115729063?v=4" alt="@rahulkr30" style="width: 300px; border-radius: 50%;" />
  <p class="light" style="text-align: center; font-size: 25px; margin: 0px;"><strong>Rahul Kumar</strong></p>
</p>

<p style="text-align: justify;" markdown>

Description of Rahul.

</p>

---

<p align="center" markdown>
{% for social in about.socials|sort(attribute="title") %}
<a href="{{ social.url }}" title="{{ social.title }}" > :{{ social.icon }}:{ .lg .light } </a>&nbsp; &nbsp;
{% endfor %}
</p>

---

<h2 class="light" align="center"><strong>Projects</strong></h2>

{% for project in about.projects %}
<div class="grid cards" markdown>
  - :{{ project.icon }}:&nbsp; **{{ project.title }}**

    <p style="text-align: justify;" markdown>
    {{ project.description }}
    </p>

    ---

    <p align=center>
    {% for link in project.links %} [:{{ link.icon }}:{ .light .secondary-hover }]({{ link.url }} "{{ link.title }}"){ target=blank_ } &nbsp; &nbsp; {% endfor %}
    </p>
</div>
{% endfor %}

<p align="center" markdown>[==All Projects==](../project/index.md)</p>

---

<h2 class="light" align="center"><strong>Tech Stacks</strong></h2>

<div class="grid cards" markdown>
{% for stack, techs in about.tech_stack.items()|sort(attribute=0) %}
  - **{{ stack }}**

    ---

    <p align="center" style="margin: 0;">
    {% for tech in techs|sort(attribute='title') %}:{{ tech.icon }}:{ .lg .hover-icon-bounce .{{ tech.icon|replace("simple-", "") }} title="{{ tech.title }}" } &nbsp; {% endfor %}
    </p>
{% endfor %}
</div>

---

<p align="center" markdown>
[:fontawesome-solid-paper-plane:{ .bounce }&nbsp; Download Resume](https://github.com/arv-anshul/arv-anshul/raw/main/resume_arv-anshul.pdf){ .md-button .md-button--primary }
</p>
