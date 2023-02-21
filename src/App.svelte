<script>

  let state = 'it̪ʰeɡʊɾmʊkʰiːlɪkʰo.'; // IPA here

  function handleClick() {

  let x =  content.innerHTML;
  state = convert(x);
  document.getElementById("content").addEventListener("input", function() {
    state = convert(x);
    }, false);
	}

  function convert(ip) {

    let prevLetter = '';
    let output = '';
    for (var i = 0; i < ip.length; i++) {
      console.log(ip.charAt(i));
      switch(ip.charAt(i)) {
        case 'ੇ':
          output += 'e'
          break;
        case 'ਾ':
        case 'ਆ':
          output += 'äː'
          break;
        case 'ਿ':
        case 'ਇ':
          output += 'ɪ'
          break;
        case 'ੀ':
        case 'ਈ':
          output += 'iː'
          break;
        case 'ੁ':
        case 'ਉ':
          output += 'ʊ'
          break;
        case 'ੂ':
        case 'ਊ':
          output += 'uː'
          break;
        case 'ੇ':
        case 'ਏ':
          output += 'e'
          break;
        case 'ੈ':
        case 'ਐ':
          output += 'ɛ'
          break;
        case 'ੋ':
        case 'ਐ':
          output += 'o'
          break;
        case 'ੌ':
        case 'ਓ':
          output += 'ɔ'
          break;
        case 'ੀ':
        case 'ਔ':
          output += 'iː'
          break;
        case '੍':
          output += ''
          break;
        case '।':
        case '।।':
          output += '.'
          break;
        case 'ਇ':
          output += 'i'
          break;
        case 'ਥ':
          output += 't̪ʰ'
          break;
        case 'ਅ':
          output += 'ə'
          break;
        case 'ਸ':
          output += 's'
          break;
        case 'ਹ':
          output += 'ɦ'
          break;
        case 'ਕ':
          output += 'k'
          break;
        case 'ਖ':
          output += 'kʰ'
          break;
        case 'ਗ':
          output += 'ɡ'
          break;
        case 'ਘ':
          output += 'gh'
          break;
        case 'ਙ':
          output += 'ŋ'
          break;
        case 'ਚ':
          output += 't͡ʃ'
          break;
        case 'ਛ':
          output += 't͡ʃʰ'
          break;
        case 'ਜ':
          output += 'd͡ʒ'
          break;
        case 'ਝ':
          output += 'jh'
          break;
        case 'ਞ':
          output += 'ɲ'
          break;
        case 'ਟ':
          output += 'ʈ'
          break;
        case 'ਠ':
          output += 'ʈʰ'
          break;
        case 'ਡ':
          output += 'ɖ'
          break;
        case 'ਢ':
          output += 'ḍh'
          break;
        case 'ਣ':
          output += 'ɳ'
          break;
        case 'ਤ':
          output += 't̪'
          break;
        case 'ਥ':
          output += 't̪ʰ'
          break;
        case 'ਦ':
          output += 'd̪'
          break;
        case 'ਧ':
          output += 'dh'
          break;
        case 'ਨ':
          output += 'n'
          break;
        case 'ਪ':
          output += 'p'
          break;
        case 'ਫ':
          output += 'pʰ'
          break;
        case 'ਬ':
          output += 'b'
          break;
        case 'ਭ':
          output += 'bh'
          break;
        case 'ਮ':
          output += 'm'
          break;
        case 'ਯ':
          output += 'j'
          break;
        case 'ਰ':
          output += 'ɾ'
          break;
        case 'ਲ':
          output += 'l'
          break;
        case 'ਵ':
          output += 'ʋ'
          break;
        case 'ੜ':
          output += 'ɽ'
          break;
        case 'ਸ਼':
          output += 'ʃ'
          break;
        case '਼':
          if (prevLetter == 'ਗ') {
            output += 'ɣ'
          }
          else if (prevLetter == 'ਲ') {
            output += 'ɭ'
          }
          else if (prevLetter == 'ਗ') {
            output += 't̪ʰ'
          }
          else if (prevLetter == 'ਖ') {
            output += 'x'
          }
          else if (prevLetter == 'ਜ') {
            output += 'z'
          }
          else if (prevLetter == 'ਫ') {
            output += 'f'
          }
          else {
            output += ''
          }
          break;
        default:
          output += ip.charAt(i)
      }
    }
    prevLetter = ip.charAt(i);
    return output;
  }

</script>



<html data-theme="retro" lang="en">
<body>
<div class="mb-10">
<h1 id="content" class="text-3xl"
on:click={handleClick}
style="height:900px;color:rgb(46 18 40);font-size: 5em;"
contenteditable='true'>
ਇਥੇਗੁਰਮੁਖੀਲਿਖੋ।
</h1>
<br />
</div>

<div style="background-color: #FDEBE8; height: 300px;
position: absolute;top:300px;padding-top: 80px; margin: auto 0; font-size: 5em;
width:100%;color:#D4BACB;">
{state}
</div>

</body>
</html>


<style>

  @media only screen and (min-width: 1100px) {
    .frame {
      border: 2px solid black;
            background-color: white;
            padding:100px;
            padding-top:20px;
            margin: 0 auto;
            width: 30%;
            margin-top:5%;
            text-align:center
    }
  }

  body {
    padding-top: 100px;
    background-color: #D986B9;
    color: rgb(240,117,110);
    text-align: center;

    font-family:monospace;

    animation: type 5s infinite;
    animation-duration: 5s;
    animation-timing-function: ease;
    animation-delay: 0s;
    animation-iteration-count: infinite;
    animation-direction: normal;
    animation-fill-mode: none;
    animation-play-state: running;
    animation-name: type;
    position: relative;
  }

  .type {
  animation: type 5s infinite;
  animation-duration: 5s;
  animation-timing-function: ease;
  animation-delay: 0s;
  animation-iteration-count: infinite;
  animation-direction: normal;
  animation-fill-mode: none;
  animation-play-state: running;
  animation-name: type;
  position: relative;
}

@keyframes type {
      0%   {
          top:0px;
      }
      100% {
          top:4px;
      }
  }

  @keyframes body {
          0%   {
              top:-4px;
          }
          100% {
              top:0px;
          }
      }

      input {
        text-align: center;
      }
  </style>
