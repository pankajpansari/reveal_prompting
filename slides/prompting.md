### Prompting Fundamentals for LLMs 

### 21 Nov, 2024
---
<section data-markdown="example.md" data-separator="^\n\n\n"
         data-separator-vertical="^\n\n" data-separator-notes="^Note:">

### The Value of Prompting Well 

Note:
- “Prompting” is how we talk to LLMs. Best way to prompt by speaking to it like you would a coworker or friend. Prompts can range from simple questions ("how do I hang a picture frame in my room?") to complex requests. 
- Most straightforward way to get value out of LLMs
- LLMs can't read minds; we need to give enough information
- As with humans so with LLMs: learning to say what we want is crucial
</section>
---
<section>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3>Prompts as Conditioning</h3>
        <aside class="notes">
        - Conditioning the probabilistic model to generate our desired output <br>
        - Conditioned the model to respond differently by adding a few tokens <br>
        </aside>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
    <div class="fragment quote-box" 
         data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="fragment quote-content" 
             data-fragment-index="2">
                <b># Prompt 1</b> <br>
                Tell me about: Apple <br><br>
                <b># Prompt 2</b><br>
                Tell me about: Apple fruit<br><br>
                <b># Prompt 3</b><br>
                Tell me about: Apple of my eye<br><br>
        </div>
    </div>
</div>
</div>
</section>
---
<section>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3> Roles and Responsibilities </h3>
        <aside class="notes">
        - Provides context that steers responses in terms of content, tone, style <br><br>
        </aside>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
    <div class="fragment quote-box" 
         data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="fragment quote-content" 
             data-fragment-index="2">
               <b># Prompt 1</b><br>
                You are a preschool teacher. Explain how attention in LLMs works.<br><br>
                <b># Prompt 2</b><br>
                You are an NLP professor. Explain how attention in LLMs works. <br><br>
               </div>
    </div>
</div>
</div>
</section>
---
<section>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3> Roles and Responsibilities </h3>
        <aside class="notes">
        Can also improve accuracy on most tasks
        </aside>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
    <div class="fragment quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="fragment quote-content" data-fragment-index="2">
                <b># Prompt 1</b><br>
                Review this code and find any issues. <br><br>
                <b># Prompt 2</b><br>
                <mark>You are a senior software security engineer </mark>specializing in code vulnerability assessment and secure coding practices. Review this code and find any issues. <br><br>
                <b># Prompt 3</b><br>
                <mark>You are responsible for ensuring </mark>this code meets industry security standards and prevents common vulnerabilities.
                Review this code and find any issues. <br><br>
               </div>
    </div>
</div>
</div>
</section>
---
<section data-auto-animate>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3> Describe the Task</h3>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
    <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2" data-id="prompt">
            <div id="typed-strings" style="display: none;">
            <p>I want you to de-identify some text by removing all personally identifiable information from it so that it can be shared safely with external organizations.<br><br>
            Here is the text you should process:<br><br>
            "Ravi is a Biology Lab Assistant at Plaksha University. He can be reached at +91 77879 93007 or ravi@plaksha.edu.in"</p>
            </div>
            <span id="typed"></span>
        </div>
    </div>
</div>
</div>
</section>
---
<section data-auto-animate>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3> Describe the Task</h3>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
    <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2" data-id="prompt">
            I want you to de-identify some text by removing all personally identifiable information from it so that it can be shared safely with external organizations.<br><br>
            <mark>**PII includes names, phone numbers, home addresses, and email addresses. Please replace all instances of PII with a singular "XXX".</mark><br><br>
            Here is the text you should process:<br><br>
            "Ravi is a Biology Lab Assistant at Plaksha University. He can be reached at +91 77879 93007 or ravi@plaksha.edu.in"
        </div>
    </div>
</div>
</div>
</section>
---
<section data-auto-animate>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3>Use XML Tags</h3>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
    <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2" data-id="prompt">
            I want you to de-identify some text by removing all personally identifiable information from it so that it can be shared safely with external organizations.<br><br>
            **PII includes names, phone numbers, home addresses, and email addresses. Please replace all instances of PII with a singular "XXX".<br><br>
            Here is the text you should process:<br><br>
            <mark><b>&lt;text &gt;</b></mark><br>
            "Ravi is a Biology Lab Assistant at Plaksha University. He can be reached at +91 77879 93007 or ravi@plaksha.edu.in"<br>
            <mark><b>&lt;\text &gt;</b></mark>
</div>
</div>
</section>
---
<section data-auto-animate>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3>Giving Examples</h3>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
    <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2">
        Here is an example:<br><br>
        &lt;example&gt;<br>
            The de-identified version of "Sohail Akbar is a cardiologist at Poseidon Hospitals Delhi. He can be reached at +91 98765-43210 or sohail.akbar@poseidon.in" would be "XXXX is a cardiologist at Apollo Hospitals Delhi. He can be reached at XXX-XXX-XXXX or XXX@XXX."<br>
        &lt;/example&gt;<br>
        </div>
    </div>
</div>
</div>
</section>
---
<section data-auto-animate>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3>Letting LLMs Think</h3>
        <aside class="notes">
        Standard approach
        </aside>
        </div>
    </div>
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
    <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2" data-id="prompt2">
        You are responsible for accurately summarizing the meeting &lt;transcript&gt;.<br><br>
        &lt;transcript&gt;<br>
        {transcript}<br>
        &lt;/transcript&gt;<br><br>
        <mark>Think step by step</mark> and return a &lt;summary&gt; of the &lt;transcript&gt;.<br>
        </div>
    </div>
    </div>
</div>
</section>
---
<section data-auto-animate>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3>Letting LLMs Think</h3>
        <aside class="notes">
        - Alternate: Contain the CoT within a designated &lt;sketchpad&gt;, and then generate &lt;summary&gt; <br><br>
        </aside>
        </div>
    </div>
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
        <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2" data-id="prompt2">
        You are responsible for accurately summarizing the meeting &lt;transcript&gt;.<br><br>
            &lt;transcript&gt;<br>
            {transcript}<br>
            &lt;/transcript&gt;<br><br>
        Think step by step on how to summarize the &lt;transcript&gt; <mark>within the provided &lt;sketchpad&gt;.</mark><br><br>
        Then, return a &lt;summary&gt; <mark>based on the &lt;sketchpad&gt;</mark>.<br><br>
        </div>
    </div>
</div>
</div>
</section>
---
<section data-auto-animate>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3>Letting LLMs Think</h3>
        <aside class="notes">
        - Even better: more specific instructions for reasoning<br><br>
        </aside>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
        <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2" data-id="prompt2">
        You are responsible for accurately summarizing the meeting &lt;transcript&gt;.<br><br>
            &lt;transcript&gt;<br>
            {transcript}<br>
            &lt;/transcript&gt;<br><br>
        Think step by step on how to summarize the &lt;transcript&gt; within the provided &lt;sketchpad&gt;.<br><br>
        In the &lt;sketchpad&gt;, <mark>return a list of &lt;decision&gt;, &lt;action_item&gt;, and &lt;owner&gt;.</mark><br><br>
        Then, check that &lt;sketchpad&gt; items <mark>are factually consistent</mark> with the &lt;transcript&gt;.<br><br>
        Finally, return a &lt;summary&gt; based on the &lt;sketchpad&gt;.<br><br>
        </div>
    </div>
</div>
</div>
</section>

---
<section>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3> Step-by-step </h3>
        <aside class="notes">
        - Refactor a large, catch-all prompt into several, single-purpose prompts <br><br>
        - Helps model focus on one task at a step; improves performance<br><br>
        </aside>
        </div>
    </div>
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
        <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2">
            You are responsible for accurately summarizing the meeting &lt;transcript&gt;.<br><br>
            &lt;transcript&gt;<br>
            {transcript}<br>
            &lt;/transcript&gt;<br><br>
            Think step by step on how to summarize the &lt;transcript&gt; within the provided &lt;sketchpad&gt;.<br><br>
            <mark>In the &lt;sketchpad&gt;, return a list of &lt;decision&gt;, &lt;action_item&gt;, and &lt;owner&gt;.</mark><br><br>
            <span style="background-color: LightPink">Then, check that &lt;sketchpad&gt; items are factually consistent with the &lt;transcript&gt;.<br><br></span>
            <span style="background-color: LightSalmon">Finally, return a &lt;summary&gt; based on the &lt;sketchpad&gt;.</span><br><br>
           </div>
    </div>
</div>
</div>
</section>
---
<section>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3> Step-by-step </h3>
        - Step 1 : Extract the decisions, action items, and owners<br><br>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
    <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
        <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2">
            <p>You are responsible for accurately summarizing the meeting &lt;transcript&gt;.<br><br>
            &lt;transcript&gt;<br>
            {transcript}<br>
            &lt;/transcript&gt;<br><br>
            From &lt;transcript&gt;, extract a list of &lt;decision&gt;, &lt;action_item&gt;, and &lt;owner&gt;. <br><br>
            Return the list within &lt;extracted_information&gt;.</p>
    </div>
    </div>
</div>
</div>
</section>
---
<section>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3> Step-by-step </h3>
        - Step 2 : Verify that the extracted items are consistent with the transcript<br><br>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
     <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
        <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2">
               You are responsible for checking &lt;extracted_information&gt; against a &lt;transcript&gt;.<br><br>
                Here is the meeting transcript:<br>
                {transcript}<br><br>
                Here is the extracted information:<br>
                {extracted_information}<br><br>
                Think step by step and check that the &lt;extracted_information&gt; is factually consistent with the &lt;transcript&gt; within the &lt;sketchpad&gt;.<br><br>
                Then, return a list of factually consistent &lt;decision&gt;, &lt;action_item&gt;, and &lt;owner&gt; within &lt;confirmed_extracted_information&gt;.<br><br>
       </div>
    </div>
</div>
</div>
</section>
---
<section>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3> Step-by-step </h3>
        - Step 3 : Format the extracted information<br><br>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
      <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
        <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2">
               You are responsible for converting &lt;information&gt; into bullet-point summaries.<br>
                &lt;information&gt;<br><br>
                {confirmed_extracted_information}<br>
                &lt;/information&gt;<br><br>
                Rewrite the &lt;information&gt; into bullets for either &lt;decision&gt; or &lt;action item&gt;, with the &lt;owner&gt; in parentheses<br>
       </div>
    </div>
</div>
</div>
</section>
---
<section>
<div class="r-stretch" style="display: flex; flex-direction: column; align-items: stretch;">
    <!-- Left column with text -->
    <div style="flex: 1; padding: 40px;">
        <div style="font-size: 0.8em; text-align: left;">
        <h3> Reducing Hallucinations</h3>
        <aside class="notes">
        - Allow LLM to say “I don’t know” or “Not applicable” <br><br>
        - Instruct model to only provide an answer if it's highly confident <br><br>
        </aside>
        </div>
    </div>
    <!-- Right column with background image and quote box -->
       <div class="image-column subtle-background" style="background-image: url('img/background.png');">
    <!-- Box container with initial size of 0 -->
        <div class="quote-box" data-fragment-index="1">
        <!-- Text that appears after box animation -->
        <div class="quote-content" data-fragment-index="2">
              Answer the following question based on the provided &lt;context&gt;. <br><br>
                &lt;context&gt; <br>
                {context} <br>
                &lt;context&gt; <br><br>
                If the question CANNOT be answered based on the &lt;context&gt;, <mark>respond with "I don't know".</mark> <br><br>
                Only provide an answer if you are <mark>highly confident</mark> it is factually correct. <br><br>
                Question: {question} <br><br>
                Answer: <br>
               </div>
    </div>
</div>
</div>
</section>
---
## Safety and Ethics 
- Privacy
- Bias
- Misinformation
- Copyright
- Carbon footprint
- Hallucination
---
## Some Thumb Rules
- Family of Models
- Context Length
- Message Limits
- Memory 
- Internet Access