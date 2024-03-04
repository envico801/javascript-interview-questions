==================== Question ====================  

### What is web speech API  

==================== Answer ====================  

Web speech API is used to enable modern browsers recognize and synthesize speech(i.e, voice data into web apps). This API has been introduced by W3C Community in the year 2012. It has two main parts,

1. **SpeechRecognition (Asynchronous Speech Recognition or Speech-to-Text):** It provides the ability to recognize voice context from an audio input and respond accordingly. This is accessed by the `SpeechRecognition` interface.

    The below example shows on how to use this API to get text from speech,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">window</span>.<span class="hljs-property">SpeechRecognition</span> = <span class="hljs-variable language_">window</span>.<span class="hljs-property">webkitSpeechRecognition</span> || <span class="hljs-variable language_">window</span>.<span class="hljs-property">SpeechRecognition</span>; <span class="hljs-comment">// webkitSpeechRecognition for Chrome and SpeechRecognition for FF</span>
<span class="hljs-keyword">const</span> recognition = <span class="hljs-keyword">new</span> <span class="hljs-variable language_">window</span>.<span class="hljs-title class_">SpeechRecognition</span>();
recognition.<span class="hljs-property">onresult</span> = <span class="hljs-function">(<span class="hljs-params">event</span>) =></span> {
  <span class="hljs-comment">// SpeechRecognitionEvent type</span>
  <span class="hljs-keyword">const</span> speechToText = event.<span class="hljs-property">results</span>[<span class="hljs-number">0</span>][<span class="hljs-number">0</span>].<span class="hljs-property">transcript</span>;
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(speechToText);
};
recognition.<span class="hljs-title function_">start</span>();
</code></pre>
<!-- codeblock-end -->

In this API, browser is going to ask you for permission to use your microphone

1. **SpeechSynthesis (Text-to-Speech):** It provides the ability to recognize voice context from an audio input and respond. This is accessed by the `SpeechSynthesis` interface.

    For example, the below code is used to get voice/speech from text,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">if</span> (<span class="hljs-string">'speechSynthesis'</span> <span class="hljs-keyword">in</span> <span class="hljs-variable language_">window</span>) {
  <span class="hljs-keyword">var</span> speech = <span class="hljs-keyword">new</span> <span class="hljs-title class_">SpeechSynthesisUtterance</span>(<span class="hljs-string">'Hello World!'</span>);
  speech.<span class="hljs-property">lang</span> = <span class="hljs-string">'en-US'</span>;
  <span class="hljs-variable language_">window</span>.<span class="hljs-property">speechSynthesis</span>.<span class="hljs-title function_">speak</span>(speech);
}
</code></pre>
<!-- codeblock-end -->

The above examples can be tested on chrome(33+) browser's developer console.

**Note:** This API is still a working draft and only available in Chrome and Firefox browsers(ofcourse Chrome only implemented the specification)

==================== Id ====================  
384

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#384-What-is-web-speech-api

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
