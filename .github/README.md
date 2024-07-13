# bookmarkletの追加方法
追加しやすいようにリンクかしたものは[ここ](https://zyagaimooisii.github.io/e-library/)←なぜかうまく動かなくなるから↓のコードを使用してください
## open-AI-iframe.js

javascript:(function()%7Bvar%20questionText=document.querySelector('.qtext-container').textContent;var%20answerElements=document.querySelectorAll('%23questionanswer-01%20li');var%20answers=%5B%5D;for(var%20i=0;i%3CanswerElements.length;i++)%7Banswers.push(answerElements%5Bi%5D.textContent);%7Dvar%20question=questionText+'%5Cn%5Cn'+answers.join(',');var%20data=%7Bquestion:question%7D;var%20iframe=document.createElement('iframe');iframe.style.position='fixed';iframe.style.top=0;iframe.style.left=0;iframe.style.width='100%25';iframe.style.height='300px';iframe.src='https://loud-changeable-bestseller.glitch.me/?question='+encodeURIComponent(question);document.body.appendChild(iframe);%7D)();

## open-AI-iframe.jsの使い方
eライブラリの問題の画面を開きながらこのブックマークレットを実行すると、ページの左上にAIのサイトがiframeで表示されます。
何も押さなくても自動的に送信してくれるので返答が来るのを待ちましょう。
エラーが返ってきた場合は時間が経ってからもう一度やると正常に返ってくることがあります。
## Show-answer-explanation.js

javascript:(function()%7B%20%20%20var%20explainText%20=%20document.getElementById('explain-dialog').textContent;%20%20%20var%20h2Elements%20=%20document.getElementsByTagName('h2');%20%20%20%20for%20(var%20i%20=%200;%20i%20%3C%20h2Elements.length;%20i++)%20%7B%20%20%20%20%20var%20h2Element%20=%20h2Elements%5Bi%5D;%20%20%20%20%20var%20newParagraph%20=%20document.createElement('p');%20%20%20%20%20newParagraph.textContent%20=%20explainText;%20%20%20%20%20h2Element.parentNode.insertBefore(newParagraph,%20h2Element.nextSibling);%20%20%20%7D%20%7D)();

## Show-answer-explanation.jsの使い方
eライブラリの問題の画面を開きながらこのブックマークレットを実行すると、本来回答が終わった後にしか見ることのできない解答解説を見ることができます。
解答解説は問題文の上に表示されます。
※数学や理科の計算のところはLaTeXが使われているので正しく表示されません。　
