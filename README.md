# bookmarkletの追加方法
## open-AI-iframe.js
[open-AI-iframe.js](javascript:(function()%7Bvar%20questionText=document.querySelector('.qtext-container').textContent;var%20answerElements=document.querySelectorAll('%23questionanswer-01%20li');var%20answers=%5B%5D;for(var%20i=0;i%3CanswerElements.length;i++)%7Banswers.push(answerElements%5Bi%5D.textContent);%7Dvar%20question=questionText+'%5Cn%5Cn'+answers.join(',');var%20data=%7Bquestion:question%7D;var%20iframe=document.createElement('iframe');iframe.style.position='fixed';iframe.style.top=0;iframe.style.left=0;iframe.style.width='100%25';iframe.style.height='300px';iframe.src='https://loud-changeable-bestseller.glitch.me/?question='+encodeURIComponent(question);document.body.appendChild(iframe);%7D)();)
## open-AI-iframe.jsの使い方
eライブラリの問題の画面を開きながらこのブックマークレットを実行すると、ページの左上にAIのサイトがiframeで表示されます。
何も押さなくても自動的に送信してくれるので返答が来るのを待ちましょう。
エラーが返ってきた場合は時間が経ってからもう一度やると正常に返ってくることがあります。
## Show-answer-explanation.jsの使い方
eライブラリの問題の画面を開きながらこのブックマークレットを実行すると、本来回答が終わった後にしか見ることのできない解答解説を見ることができます。
解答解説は問題文の上に表示されます。
※数学や理科の計算のところはLaTeXが使われているので正しく表示されません。　
