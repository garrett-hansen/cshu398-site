<h2 align="center"><b>Overview</b></h2>
Natural language processing is a field of computer science research in which machine learning or artificial intelligence programs are utilized to attempt to understand inputs from humans naturally.
A modern application of this field is in developing tools which can take in a human’s description of a module of code and produce an actual implementation of the code based on the description as well as any other available context within a file.
The objective of these applications is to allow software developers to cut down on implementation time in the development of an application, while benefitting from spending more time documenting code functionality.

<h2 align="center"><b>Terminology</b></h2>
<b>Application Programming Interface (API):</b>
An application that provides some sort of data or functionality to another application, usually through some sort of communication protocol.

<b>Generated Pre-trained Transformer 2 (GPT-2):</b>
An artificial intelligence model that can generate relevant text responses to an input of text

<b>Microsoft Visual Studio Code (VSCode):</b>
A highly modifiable and extensible program widely used by software developers to write software programs.

<h2 align="center"><b>GPT Code Clippy</b></h2>
GPT-Code-Clippy is one such artificial intelligence helper. It runs on a technology known as GPT-2, a large-scale model of publicly available online content and text. GPT-Code-Clippy uses GPT-2 models as a training set, primarily from publicly available GitHub repositories, to allow researchers and developers to generate relevant code output suggestions for given input [1].
This means that suggestions that the program provides are usually higher quality because the training set is primarily made up of real-world code samples and not just text that may or may not have as much relevancy to code development. 
GPT-Code-Clippy is available as an open source extension for VSCode but is very early in development compared to some competitors, such as GitHub CoPilot. However, it's an open source program, meaning it’s easier to understand how the extension operates for the sake of research. It must be noted that the extension is currently only available in the Insider’s Edition of VSCode [2], which is an early-release version of VSCode that isn’t as popular because it isn’t always a stable application.
I believe that this is a problem that needs to be solved if this AI helper wants to grow in popularity, since it doesn’t run on a stable VSCode version that many software developers use. The out-of-the-box version of GPT-Code-Clippy provides support for a small selection of trained GPT-2 models from what’s known a third party API known as Accelerated Inference [2]. In my testing of the program, I used one of the models provided from this API, although it has a relatively low free-usage limit before payments have to be made in order to continue using the API [4]. Because GPT-Code-Clippy is open-source, it is possible for a developer to host a training model locally on their own computer and query against that model rather than using the Accelerated Inference API if they wanted to, thus avoiding the need to pay for usage of the third-party API. For the scope of this project, I didn’t need to do this, but a developer that would want to utilize this program for longer than a month or would need to consider it.

<h2 align="center"><b>Experimentation: What Worked & What Didn’t</b></h2>
Before I could start experimenting with GPT-Code-Clippy, I had to come up with a way of measuring how successful the outcomes of my experiments were.
After all, natural language processing is a complex subject, and even GitHub CoPilot, which is possibly the most sophisticated artificial intelligence helper available today, only claims to have a success rate of 43-57% for passing benchmark tests successfully for writing code modules with well defined resolutions [3]. I wasn’t sure how I could come up with a set of benchmark tests that made a lot of sense and could be reasonably and objectively defined in the scope of this project, but I can talk about some of my observations about how changing code affected the success rate of using this application to make code suggestions.

From testing the program with my own benchmark, I found that the program’s ability to output successful and relevant results heavily depends on a few things:
Content of the file - the program creates a context of the file by reading it’s contents, so it’s easier to get accurate outcomes from the program by accurately describing other parts of a file as well, and not just the functions that you want the program to write.
Length of the file - Because the program uses the entire file context, I noticed that the code suggestions became less and less accurate and more gibberish in longer files of code. I observed a sharp decrease in the accuracy of suggestions in files more than a couple hundred lines of code.
Complexity of desired code - I found that the accuracy of the suggestions depended on how many desired inputs and operations a function should need to have. The program consistently struggled with suggesting accurate output for even well-described but lengthy or complex functions.

<h2 align="center"><b>Concluding Thoughts</b></h2>
I’m really glad that I chose to do research into using this program and the underlying information behind it and other programs like it. Natural language processing is a pretty cool field in Computer Science that I don’t have a lot of knowledge about, so it was nice to get my hands on a product of it and play with it and see how it works. Admittedly I found the program too unreliable to be worth using for any serious development in it’s current state, especially given the amount of effort necessary to even get the program running and how early in development it is, but it could potentially be useful as a learning tool for anyone new to programming. I imagine that there could be some sort of application for GPT-Code-Clippy or programs like it in controlled environments to help new programmers out, since they usually start out by working on very simple programs. This sort of program could be used by new programmers to produce code based on what they’d like to do, which might help generate real code samples of work that they’d like so that they can learn by example. 


<h2 align="center"><b>Sources</b></h2>
[1] https://openai.com/blog/better-language-models/

[2] https://github.com/CodedotAl/code-clippy-vscode

[3] https://copilot.github.com/#faq-how-good-is-github-copilot

[4] https://huggingface.co/pricing


