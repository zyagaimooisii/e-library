# bookmarkletの追加方法
## open-AI-iframe.js
[open-AI-iframe.js](javascript:(function()%7Bjavascript%3A(function()%257Bvar%2520questionText%3Ddocument.querySelector('.qtext-container').textContent%3Bvar%2520answerElements%3Ddocument.querySelectorAll('%2523questionanswer-01%2520li')%3Bvar%2520answers%3D%255B%255D%3Bfor(var%2520i%3D0%3Bi%253CanswerElements.length%3Bi%2B%2B)%257Banswers.push(answerElements%255Bi%255D.textContent)%3B%257Dvar%2520question%3DquestionText%2B'%255Cn%255Cn'%2Banswers.join('%2C')%3Bvar%2520data%3D%257Bquestion%3Aquestion%257D%3Bvar%2520iframe%3Ddocument.createElement('iframe')%3Biframe.style.position%3D'fixed'%3Biframe.style.top%3D0%3Biframe.style.left%3D0%3Biframe.style.width%3D'100%2525'%3Biframe.style.height%3D'300px'%3Biframe.src%3D'https%3A%2F%2Floud-changeable-bestseller.glitch.me%2F%3Fquestion%3D'%2BencodeURIComponent(question)%3Bdocument.body.appendChild(iframe)%3B%257D)()%7D)())
## open-AI-iframe.jsの使い方
eライブラリの問題の画面を開きながらこのブックマークレットを実行すると、ページの左上にAIのサイトがiframeで表示されます。
何も押さなくても自動的に送信してくれるので返答が来るのを待ちましょう。
エラーが返ってきた場合は時間が経ってからもう一度やると正常に返ってくることがあります。
## Show-answer-explanation.jsの使い方
eライブラリの問題の画面を開きながらこのブックマークレットを実行すると、本来回答が終わった後にしか見ることのできない解答解説を見ることができます。
解答解説は問題文の上に表示されます。
※数学や理科の計算のところはLaTeXが使われているので正しく表示されません。　
