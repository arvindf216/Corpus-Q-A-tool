Corpus Q&A Tool

Write all queries in the text file queries.txt. It already contains 5 sample queries.

Run the following command on the terminal: 
-  For LINUX: g++ Node.cpp dict.cpp search.cpp qna_tool.cpp new_tester.cpp 
-  For Windows: g++ Node.cpp dict.cpp search.cpp qna_tool.cpp new_tester.cpp

The above command compiles all the required files into an executable by the name a.out for LINUX and a.exe for Windows.

To execute the created file:
-  For LINUX: ./a.out
-  For Windows: ./a.exe

You will soon be able to see the answers to the questions asked!

P.S. - Do read report.pdf to know more about this project!

NOTE:

- The corpus directory contains all 98 volumes of the Complete Works of Mahatma Gandhi, so the program is currently capable of answering any question from the life of Mahatma Gandhi whose answer is present in the mentioned set of books.

- Also, the program is written assuming that all the books of the corpus have their filename in the format, "corpus/mahatma-gandhi-collected-works-volume-<Book_Code>.txt" 

- The program is already fed with API_KEYS and/or login credentials for all the APIS, ChatGPT, HuggingChat, Google PaLM API

- The program then determines the top k (currently set to 5) paragraphs relevant to the question which is then fed to ChatGPT and PaLM and then both their outputs are given to HuggingChat which generates the final output answer displayed to the user.
(Since the program makes use of APIs it needs to connect to the internet and retrieve data. So, it takes some time for the program to complete execution.)

---> The program generates files, 
1.  query.txt which contains the top-k paragraphs determined with the question asked, which in its entirety is fed to the LLM
2.  hug_query.txt, the text that is asked to HuggingChat to retreive the final output, contains the answers from ChatGPT and PaLM
