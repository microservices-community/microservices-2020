## Submission

{% assign status = 1 %}

A submission should describe a talk to be given at the conference in the form of extended abstracts with a maximum of **two pages**. 

Submissions can be based on work in progress, scientific work published or submitted for publication, practical experience reports, or practical tool demonstrations. 

They must be prepared using the **EasyChair template** ([LaTeX](https://www.easychair.org/publications/easychair.zip), [MS Word](https://www.easychair.org/publications/easychair.docx)), be in PDF format, printable in black and white on A4 paper, and interpretable by common PDF tools. Submissions must be in English.

Contributions will be reviewed and selected by the [Program Committee]({{ '/committees/' | relative_url }}). Extended abstracts of accepted contributions will be available electronically before the conference.

{% if status > 0 %}
Contributions may be submitted via EasyChair by clicking the button below. The submission deadline is **June 10th, 2020** <acronym title="Anywhere on earth">AoE</acronym>. Resubmissions are allowed until the submission deadline.
{% endif %}

For more details on the conference's scope and topics see the <a class="link-to-tab" href="#call-for-papers">call for papers</a>.

{% case status %}
{% when 0 %}
<p style="margin:2em;" class="text-center">
    <button style="padding:1em;" type="button" class="btn btn-primary btn-lg disabled">The submission system is not open yet</button>
</p>
{% when 1 %}
<p style="margin:2em;" class="text-center">
    <a href="https://easychair.org/my/conference?conf=microservices2020"><button style="padding:1em;" type="button" class="btn btn-primary btn-lg">Submit</button></a>
</p>
{% else %}
<p style="margin:2em;" class="text-center">
    <button style="padding:1em;" type="button" class="btn btn-primary btn-lg disabled">The submission system is closed</button>
</p>
{% endcase %}
