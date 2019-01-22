<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>RocketFuelCaseStudy</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*//*! normalize.css v3.0.2 | MIT License | git.io/normalize */html{font-family:sans-serif;-ms-text-size-adjust:100%;-webkit-text-size-adjust:100%;font-size:10px;-webkit-tap-highlight-color:transparent}article,aside,details,figcaption,figure,footer,header,hgroup,main,menu,nav,section,summary{display:block}audio,canvas,progress,video{display:inline-block;vertical-align:baseline}audio:not([controls]){display:none;height:0}[hidden],template{display:none}a{background-color:transparent}a:active,a:hover{outline:0}abbr[title]{border-bottom:1px dotted}b,optgroup,strong{font-weight:700}dfn{font-style:italic}h1{font-size:2em;margin:.67em 0}mark{background:#ff0;color:#000}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sup{top:-.5em}sub{bottom:-.25em}img{border:0;vertical-align:middle}svg:not(:root){overflow:hidden}hr{-moz-box-sizing:content-box;box-sizing:content-box;height:0}pre,textarea{overflow:auto}code,kbd,pre,samp{font-size:1em}button,input,optgroup,select,textarea{color:inherit;font:inherit;margin:0}button{overflow:visible}button,select{text-transform:none}button,html input[type=button],input[type=reset],input[type=submit]{-webkit-appearance:button;cursor:pointer}button[disabled],html input[disabled]{cursor:default}button::-moz-focus-inner,input::-moz-focus-inner{border:0;padding:0}input{line-height:normal}input[type=checkbox],input[type=radio]{box-sizing:border-box;padding:0}input[type=number]::-webkit-inner-spin-button,input[type=number]::-webkit-outer-spin-button{height:auto}input[type=search]::-webkit-search-cancel-button,input[type=search]::-webkit-search-decoration{-webkit-appearance:none}table{border-collapse:collapse;border-spacing:0}td,th{padding:0}/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */@media print{*,:after,:before{background:0 0!important;color:#000!important;box-shadow:none!important;text-shadow:none!important}a,a:visited{text-decoration:underline}a[href]:after{content:" (" attr(href)")"}abbr[title]:after{content:" (" attr(title)")"}a[href^="javascript:"]:after,a[href^="#"]:after{content:""}blockquote,pre{border:1px solid #999;page-break-inside:avoid}thead{display:table-header-group}img,tr{page-break-inside:avoid}img{max-width:100%!important}h2,h3,p{orphans:3;widows:3}h2,h3{page-break-after:avoid}select{background:#fff!important}.navbar{display:none}.btn>.caret,.dropup>.btn>.caret{border-top-color:#000!important}.label{border:1px solid #000}.table{border-collapse:collapse!important}.table td,.table th{background-color:#fff!important}.table-bordered td,.table-bordered th{border:1px solid #ddd!important}}@font-face{font-family:'Glyphicons Halflings';src:url(../components/bootstrap/fonts/glyphicons-halflings-regular.eot);src:url(../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix)format('embedded-opentype'),url(../components/bootstrap/fonts/glyphicons-halflings-regular.woff2)format('woff2'),url(../components/bootstrap/fonts/glyphicons-halflings-regular.woff)format('woff'),url(../components/bootstrap/fonts/glyphicons-halflings-regular.ttf)format('truetype'),url(../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular)format('svg')}.glyphicon{position:relative;top:1px;display:inline-block;font-family:'Glyphicons Halflings';font-style:normal;font-weight:400;line-height:1;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale}.glyphicon-asterisk:before{content:"\2a"}.glyphicon-plus:before{content:"\2b"}.glyphicon-eur:before,.glyphicon-euro:before{content:"\20ac"}.glyphicon-minus:before{content:"\2212"}.glyphicon-cloud:before{content:"\2601"}.glyphicon-envelope:before{content:"\2709"}.glyphicon-pencil:before{content:"\270f"}.glyphicon-glass:before{content:"\e001"}.glyphicon-music:before{content:"\e002"}.glyphicon-search:before{content:"\e003"}.glyphicon-heart:before{content:"\e005"}.glyphicon-star:before{content:"\e006"}.glyphicon-star-empty:before{content:"\e007"}.glyphicon-user:before{content:"\e008"}.glyphicon-film:before{content:"\e009"}.glyphicon-th-large:before{content:"\e010"}.glyphicon-th:before{content:"\e011"}.glyphicon-th-list:before{content:"\e012"}.glyphicon-ok:before{content:"\e013"}.glyphicon-remove:before{content:"\e014"}.glyphicon-zoom-in:before{content:"\e015"}.glyphicon-zoom-out:before{content:"\e016"}.glyphicon-off:before{content:"\e017"}.glyphicon-signal:before{content:"\e018"}.glyphicon-cog:before{content:"\e019"}.glyphicon-trash:before{content:"\e020"}.glyphicon-home:before{content:"\e021"}.glyphicon-file:before{content:"\e022"}.glyphicon-time:before{content:"\e023"}.glyphicon-road:before{content:"\e024"}.glyphicon-download-alt:before{content:"\e025"}.glyphicon-download:before{content:"\e026"}.glyphicon-upload:before{content:"\e027"}.glyphicon-inbox:before{content:"\e028"}.glyphicon-play-circle:before{content:"\e029"}.glyphicon-repeat:before{content:"\e030"}.glyphicon-refresh:before{content:"\e031"}.glyphicon-list-alt:before{content:"\e032"}.glyphicon-lock:before{content:"\e033"}.glyphicon-flag:before{content:"\e034"}.glyphicon-headphones:before{content:"\e035"}.glyphicon-volume-off:before{content:"\e036"}.glyphicon-volume-down:before{content:"\e037"}.glyphicon-volume-up:before{content:"\e038"}.glyphicon-qrcode:before{content:"\e039"}.glyphicon-barcode:before{content:"\e040"}.glyphicon-tag:before{content:"\e041"}.glyphicon-tags:before{content:"\e042"}.glyphicon-book:before{content:"\e043"}.glyphicon-bookmark:before{content:"\e044"}.glyphicon-print:before{content:"\e045"}.glyphicon-camera:before{content:"\e046"}.glyphicon-font:before{content:"\e047"}.glyphicon-bold:before{content:"\e048"}.glyphicon-italic:before{content:"\e049"}.glyphicon-text-height:before{content:"\e050"}.glyphicon-text-width:before{content:"\e051"}.glyphicon-align-left:before{content:"\e052"}.glyphicon-align-center:before{content:"\e053"}.glyphicon-align-right:before{content:"\e054"}.glyphicon-align-justify:before{content:"\e055"}.glyphicon-list:before{content:"\e056"}.glyphicon-indent-left:before{content:"\e057"}.glyphicon-indent-right:before{content:"\e058"}.glyphicon-facetime-video:before{content:"\e059"}.glyphicon-picture:before{content:"\e060"}.glyphicon-map-marker:before{content:"\e062"}.glyphicon-adjust:before{content:"\e063"}.glyphicon-tint:before{content:"\e064"}.glyphicon-edit:before{content:"\e065"}.glyphicon-share:before{content:"\e066"}.glyphicon-check:before{content:"\e067"}.glyphicon-move:before{content:"\e068"}.glyphicon-step-backward:before{content:"\e069"}.glyphicon-fast-backward:before{content:"\e070"}.glyphicon-backward:before{content:"\e071"}.glyphicon-play:before{content:"\e072"}.glyphicon-pause:before{content:"\e073"}.glyphicon-stop:before{content:"\e074"}.glyphicon-forward:before{content:"\e075"}.glyphicon-fast-forward:before{content:"\e076"}.glyphicon-step-forward:before{content:"\e077"}.glyphicon-eject:before{content:"\e078"}.glyphicon-chevron-left:before{content:"\e079"}.glyphicon-chevron-right:before{content:"\e080"}.glyphicon-plus-sign:before{content:"\e081"}.glyphicon-minus-sign:before{content:"\e082"}.glyphicon-remove-sign:before{content:"\e083"}.glyphicon-ok-sign:before{content:"\e084"}.glyphicon-question-sign:before{content:"\e085"}.glyphicon-info-sign:before{content:"\e086"}.glyphicon-screenshot:before{content:"\e087"}.glyphicon-remove-circle:before{content:"\e088"}.glyphicon-ok-circle:before{content:"\e089"}.glyphicon-ban-circle:before{content:"\e090"}.glyphicon-arrow-left:before{content:"\e091"}.glyphicon-arrow-right:before{content:"\e092"}.glyphicon-arrow-up:before{content:"\e093"}.glyphicon-arrow-down:before{content:"\e094"}.glyphicon-share-alt:before{content:"\e095"}.glyphicon-resize-full:before{content:"\e096"}.glyphicon-resize-small:before{content:"\e097"}.glyphicon-exclamation-sign:before{content:"\e101"}.glyphicon-gift:before{content:"\e102"}.glyphicon-leaf:before{content:"\e103"}.glyphicon-fire:before{content:"\e104"}.glyphicon-eye-open:before{content:"\e105"}.glyphicon-eye-close:before{content:"\e106"}.glyphicon-warning-sign:before{content:"\e107"}.glyphicon-plane:before{content:"\e108"}.glyphicon-calendar:before{content:"\e109"}.glyphicon-random:before{content:"\e110"}.glyphicon-comment:before{content:"\e111"}.glyphicon-magnet:before{content:"\e112"}.glyphicon-chevron-up:before{content:"\e113"}.glyphicon-chevron-down:before{content:"\e114"}.glyphicon-retweet:before{content:"\e115"}.glyphicon-shopping-cart:before{content:"\e116"}.glyphicon-folder-close:before{content:"\e117"}.glyphicon-folder-open:before{content:"\e118"}.glyphicon-resize-vertical:before{content:"\e119"}.glyphicon-resize-horizontal:before{content:"\e120"}.glyphicon-hdd:before{content:"\e121"}.glyphicon-bullhorn:before{content:"\e122"}.glyphicon-bell:before{content:"\e123"}.glyphicon-certificate:before{content:"\e124"}.glyphicon-thumbs-up:before{content:"\e125"}.glyphicon-thumbs-down:before{content:"\e126"}.glyphicon-hand-right:before{content:"\e127"}.glyphicon-hand-left:before{content:"\e128"}.glyphicon-hand-up:before{content:"\e129"}.glyphicon-hand-down:before{content:"\e130"}.glyphicon-circle-arrow-right:before{content:"\e131"}.glyphicon-circle-arrow-left:before{content:"\e132"}.glyphicon-circle-arrow-up:before{content:"\e133"}.glyphicon-circle-arrow-down:before{content:"\e134"}.glyphicon-globe:before{content:"\e135"}.glyphicon-wrench:before{content:"\e136"}.glyphicon-tasks:before{content:"\e137"}.glyphicon-filter:before{content:"\e138"}.glyphicon-briefcase:before{content:"\e139"}.glyphicon-fullscreen:before{content:"\e140"}.glyphicon-dashboard:before{content:"\e141"}.glyphicon-paperclip:before{content:"\e142"}.glyphicon-heart-empty:before{content:"\e143"}.glyphicon-link:before{content:"\e144"}.glyphicon-phone:before{content:"\e145"}.glyphicon-pushpin:before{content:"\e146"}.glyphicon-usd:before{content:"\e148"}.glyphicon-gbp:before{content:"\e149"}.glyphicon-sort:before{content:"\e150"}.glyphicon-sort-by-alphabet:before{content:"\e151"}.glyphicon-sort-by-alphabet-alt:before{content:"\e152"}.glyphicon-sort-by-order:before{content:"\e153"}.glyphicon-sort-by-order-alt:before{content:"\e154"}.glyphicon-sort-by-attributes:before{content:"\e155"}.glyphicon-sort-by-attributes-alt:before{content:"\e156"}.glyphicon-unchecked:before{content:"\e157"}.glyphicon-expand:before{content:"\e158"}.glyphicon-collapse-down:before{content:"\e159"}.glyphicon-collapse-up:before{content:"\e160"}.glyphicon-log-in:before{content:"\e161"}.glyphicon-flash:before{content:"\e162"}.glyphicon-log-out:before{content:"\e163"}.glyphicon-new-window:before{content:"\e164"}.glyphicon-record:before{content:"\e165"}.glyphicon-save:before{content:"\e166"}.glyphicon-open:before{content:"\e167"}.glyphicon-saved:before{content:"\e168"}.glyphicon-import:before{content:"\e169"}.glyphicon-export:before{content:"\e170"}.glyphicon-send:before{content:"\e171"}.glyphicon-floppy-disk:before{content:"\e172"}.glyphicon-floppy-saved:before{content:"\e173"}.glyphicon-floppy-remove:before{content:"\e174"}.glyphicon-floppy-save:before{content:"\e175"}.glyphicon-floppy-open:before{content:"\e176"}.glyphicon-credit-card:before{content:"\e177"}.glyphicon-transfer:before{content:"\e178"}.glyphicon-cutlery:before{content:"\e179"}.glyphicon-header:before{content:"\e180"}.glyphicon-compressed:before{content:"\e181"}.glyphicon-earphone:before{content:"\e182"}.glyphicon-phone-alt:before{content:"\e183"}.glyphicon-tower:before{content:"\e184"}.glyphicon-stats:before{content:"\e185"}.glyphicon-sd-video:before{content:"\e186"}.glyphicon-hd-video:before{content:"\e187"}.glyphicon-subtitles:before{content:"\e188"}.glyphicon-sound-stereo:before{content:"\e189"}.glyphicon-sound-dolby:before{content:"\e190"}.glyphicon-sound-5-1:before{content:"\e191"}.glyphicon-sound-6-1:before{content:"\e192"}.glyphicon-sound-7-1:before{content:"\e193"}.glyphicon-copyright-mark:before{content:"\e194"}.glyphicon-registration-mark:before{content:"\e195"}.glyphicon-cloud-download:before{content:"\e197"}.glyphicon-cloud-upload:before{content:"\e198"}.glyphicon-tree-conifer:before{content:"\e199"}.glyphicon-tree-deciduous:before{content:"\e200"}.glyphicon-cd:before{content:"\e201"}.glyphicon-save-file:before{content:"\e202"}.glyphicon-open-file:before{content:"\e203"}.glyphicon-level-up:before{content:"\e204"}.glyphicon-copy:before{content:"\e205"}.glyphicon-paste:before{content:"\e206"}.glyphicon-alert:before{content:"\e209"}.glyphicon-equalizer:before{content:"\e210"}.glyphicon-king:before{content:"\e211"}.glyphicon-queen:before{content:"\e212"}.glyphicon-pawn:before{content:"\e213"}.glyphicon-bishop:before{content:"\e214"}.glyphicon-knight:before{content:"\e215"}.glyphicon-baby-formula:before{content:"\e216"}.glyphicon-tent:before{content:"\26fa"}.glyphicon-blackboard:before{content:"\e218"}.glyphicon-bed:before{content:"\e219"}.glyphicon-apple:before{content:"\f8ff"}.glyphicon-erase:before{content:"\e221"}.glyphicon-hourglass:before{content:"\231b"}.glyphicon-lamp:before{content:"\e223"}.glyphicon-duplicate:before{content:"\e224"}.glyphicon-piggy-bank:before{content:"\e225"}.glyphicon-scissors:before{content:"\e226"}.glyphicon-bitcoin:before,.glyphicon-btc:before,.glyphicon-xbt:before{content:"\e227"}.glyphicon-jpy:before,.glyphicon-yen:before{content:"\00a5"}.glyphicon-rub:before,.glyphicon-ruble:before{content:"\20bd"}.glyphicon-scale:before{content:"\e230"}.glyphicon-ice-lolly:before{content:"\e231"}.glyphicon-ice-lolly-tasted:before{content:"\e232"}.glyphicon-education:before{content:"\e233"}.glyphicon-option-horizontal:before{content:"\e234"}.glyphicon-option-vertical:before{content:"\e235"}.glyphicon-menu-hamburger:before{content:"\e236"}.glyphicon-modal-window:before{content:"\e237"}.glyphicon-oil:before{content:"\e238"}.glyphicon-grain:before{content:"\e239"}.glyphicon-sunglasses:before{content:"\e240"}.glyphicon-text-size:before{content:"\e241"}.glyphicon-text-color:before{content:"\e242"}.glyphicon-text-background:before{content:"\e243"}.glyphicon-object-align-top:before{content:"\e244"}.glyphicon-object-align-bottom:before{content:"\e245"}.glyphicon-object-align-horizontal:before{content:"\e246"}.glyphicon-object-align-left:before{content:"\e247"}.glyphicon-object-align-vertical:before{content:"\e248"}.glyphicon-object-align-right:before{content:"\e249"}.glyphicon-triangle-right:before{content:"\e250"}.glyphicon-triangle-left:before{content:"\e251"}.glyphicon-triangle-bottom:before{content:"\e252"}.glyphicon-triangle-top:before{content:"\e253"}.glyphicon-console:before{content:"\e254"}.glyphicon-superscript:before{content:"\e255"}.glyphicon-subscript:before{content:"\e256"}.glyphicon-menu-left:before{content:"\e257"}.glyphicon-menu-right:before{content:"\e258"}.glyphicon-menu-down:before{content:"\e259"}.glyphicon-menu-up:before{content:"\e260"}*,:after,:before{-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box}body{margin:0;font-family:"Helvetica Neue",Helvetica,Arial,sans-serif;font-size:13px;line-height:1.42857143;color:#000;background-color:#fff}button,input,select,textarea{font-family:inherit;font-size:inherit;line-height:inherit}a{color:#337ab7;text-decoration:none}a:focus,a:hover{color:#23527c;text-decoration:underline}a:focus{outline:dotted thin;outline:-webkit-focus-ring-color auto 5px;outline-offset:-2px}figure{margin:0}.carousel-inner>.item>a>img,.carousel-inner>.item>img,.img-responsive,.thumbnail a>img,.thumbnail>img{display:block;max-width:100%;height:auto}.img-rounded{border-radius:3px}.img-thumbnail{padding:4px;line-height:1.42857143;background-color:#fff;border:1px solid #ddd;border-radius:2px;-webkit-transition:all .2s ease-in-out;-o-transition:all .2s ease-in-out;transition:all .2s ease-in-out;display:inline-block;max-width:100%;height:auto}.img-circle{border-radius:50%}hr{margin-top:18px;margin-bottom:18px;border:0;border-top:1px solid #eee}.sr-only{position:absolute;width:1px;height:1px;margin:-1px;padding:0;overflow:hidden;clip:rect(0,0,0,0);border:0}.sr-only-focusable:active,.sr-only-focusable:focus{position:static;width:auto;height:auto;margin:0;overflow:visible;clip:auto}[role=button]{cursor:pointer}.h1,.h2,.h3,.h4,.h5,.h6,h1,h2,h3,h4,h5,h6{font-family:inherit;font-weight:500;line-height:1.1;color:inherit}.h1 .small,.h1 small,.h2 .small,.h2 small,.h3 .small,.h3 small,.h4 .small,.h4 small,.h5 .small,.h5 small,.h6 .small,.h6 small,h1 .small,h1 small,h2 .small,h2 small,h3 .small,h3 small,h4 .small,h4 small,h5 .small,h5 small,h6 .small,h6 small{font-weight:400;line-height:1;color:#777}.h1,.h2,.h3,h1,h2,h3{margin-top:18px;margin-bottom:9px}.h1 .small,.h1 small,.h2 .small,.h2 small,.h3 .small,.h3 small,h1 .small,h1 small,h2 .small,h2 small,h3 .small,h3 small{font-size:65%}.h4,.h5,.h6,h4,h5,h6{margin-top:9px;margin-bottom:9px}.h4 .small,.h4 small,.h5 .small,.h5 small,.h6 .small,.h6 small,h4 .small,h4 small,h5 .small,h5 small,h6 .small,h6 small{font-size:75%}.h1,h1{font-size:33px}.h2,h2{font-size:27px}.h3,h3{font-size:23px}.h4,h4{font-size:17px}.h5,h5{font-size:13px}.h6,h6{font-size:12px}p{margin:0 0 9px}.lead{margin-bottom:18px;font-size:14px;font-weight:300;line-height:1.4}@media (min-width:768px){.lead{font-size:19.5px}}.small,small{font-size:92%}.mark,mark{background-color:#fcf8e3;padding:.2em}.text-left{text-align:left}.text-right{text-align:right}.text-center{text-align:center}.text-justify{text-align:justify}.text-nowrap{white-space:nowrap}.text-lowercase{text-transform:lowercase}.text-uppercase{text-transform:uppercase}.text-capitalize{text-transform:capitalize}.text-muted{color:#777}.text-primary{color:#337ab7}a.text-primary:hover{color:#286090}.text-success{color:#3c763d}a.text-success:hover{color:#2b542c}.text-info{color:#31708f}a.text-info:hover{color:#245269}.text-warning{color:#8a6d3b}a.text-warning:hover{color:#66512c}.text-danger{color:#a94442}a.text-danger:hover{color:#843534}.bg-primary{color:#fff;background-color:#337ab7}a.bg-primary:hover{background-color:#286090}.bg-success{background-color:#dff0d8}a.bg-success:hover{background-color:#c1e2b3}.bg-info{background-color:#d9edf7}a.bg-info:hover{background-color:#afd9ee}.bg-warning{background-color:#fcf8e3}a.bg-warning:hover{background-color:#f7ecb5}.bg-danger{background-color:#f2dede}a.bg-danger:hover{background-color:#e4b9b9}.page-header{padding-bottom:8px;margin:36px 0 18px;border-bottom:1px solid #eee}ol,ul{margin-top:0;margin-bottom:9px}ol ol,ol ul,ul ol,ul ul{margin-bottom:0}.list-unstyled{padding-left:0;list-style:none}.list-inline{padding-left:0;list-style:none;margin-left:-5px}.list-inline>li{display:inline-block;padding-left:5px;padding-right:5px}dl{margin-top:0;margin-bottom:18px}dd,dt{line-height:1.42857143}dt{font-weight:700}dd{margin-left:0}@media (min-width:541px){.dl-horizontal dt{float:left;width:160px;clear:left;text-align:right;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}.dl-horizontal dd{margin-left:180px}}abbr[data-original-title],abbr[title]{cursor:help;border-bottom:1px dotted #777}.initialism{font-size:90%;text-transform:uppercase}blockquote{padding:9px 18px;margin:0 0 18px;font-size:inherit;border-left:5px solid #eee}blockquote ol:last-child,blockquote p:last-child,blockquote ul:last-child{margin-bottom:0}blockquote .small,blockquote footer,blockquote small{display:block;font-size:80%;line-height:1.42857143;color:#777}blockquote .small:before,blockquote footer:before,blockquote small:before{content:'\2014 \00A0'}.blockquote-reverse,blockquote.pull-right{padding-right:15px;padding-left:0;border-right:5px solid #eee;border-left:0;text-align:right}.blockquote-reverse .small:before,.blockquote-reverse footer:before,.blockquote-reverse small:before,blockquote.pull-right .small:before,blockquote.pull-right footer:before,blockquote.pull-right small:before{content:''}.blockquote-reverse .small:after,.blockquote-reverse footer:after,.blockquote-reverse small:after,blockquote.pull-right .small:after,blockquote.pull-right footer:after,blockquote.pull-right small:after{content:'\00A0 \2014'}address{margin-bottom:18px;font-style:normal;line-height:1.42857143}code,kbd,pre,samp{font-family:monospace}code{padding:2px 4px;font-size:90%;background-color:#f9f2f4;border-radius:2px}kbd{padding:2px 4px;font-size:90%;color:#fff;background-color:#333;border-radius:1px;box-shadow:inset 0 -1px 0 rgba(0,0,0,.25)}kbd kbd{padding:0;font-size:100%;font-weight:700;box-shadow:none}pre{display:block;padding:8.5px;margin:0 0 9px;word-break:break-all;word-wrap:break-word;color:#333;background-color:#f5f5f5;border:1px solid #ccc;border-radius:2px}pre code{padding:0;font-size:inherit;color:inherit;white-space:pre-wrap;background-color:transparent;border-radius:0}.pre-scrollable{max-height:340px;overflow-y:scroll}.container{margin-right:auto;margin-left:auto;padding-left:0;padding-right:0}@media (min-width:768px){.container{width:768px}}@media (min-width:992px){.container{width:940px}}@media (min-width:1200px){.container{width:1140px}}.container-fluid{margin-right:auto;margin-left:auto;padding-left:0;padding-right:0}.row{margin-left:0;margin-right:0}.col-lg-1,.col-lg-10,.col-lg-11,.col-lg-12,.col-lg-2,.col-lg-3,.col-lg-4,.col-lg-5,.col-lg-6,.col-lg-7,.col-lg-8,.col-lg-9,.col-md-1,.col-md-10,.col-md-11,.col-md-12,.col-md-2,.col-md-3,.col-md-4,.col-md-5,.col-md-6,.col-md-7,.col-md-8,.col-md-9,.col-sm-1,.col-sm-10,.col-sm-11,.col-sm-12,.col-sm-2,.col-sm-3,.col-sm-4,.col-sm-5,.col-sm-6,.col-sm-7,.col-sm-8,.col-sm-9,.col-xs-1,.col-xs-10,.col-xs-11,.col-xs-12,.col-xs-2,.col-xs-3,.col-xs-4,.col-xs-5,.col-xs-6,.col-xs-7,.col-xs-8,.col-xs-9{position:relative;min-height:1px;padding-left:0;padding-right:0}.col-xs-1,.col-xs-10,.col-xs-11,.col-xs-12,.col-xs-2,.col-xs-3,.col-xs-4,.col-xs-5,.col-xs-6,.col-xs-7,.col-xs-8,.col-xs-9{float:left}.col-xs-12{width:100%}.col-xs-11{width:91.66666667%}.col-xs-10{width:83.33333333%}.col-xs-9{width:75%}.col-xs-8{width:66.66666667%}.col-xs-7{width:58.33333333%}.col-xs-6{width:50%}.col-xs-5{width:41.66666667%}.col-xs-4{width:33.33333333%}.col-xs-3{width:25%}.col-xs-2{width:16.66666667%}.col-xs-1{width:8.33333333%}.col-xs-pull-12{right:100%}.col-xs-pull-11{right:91.66666667%}.col-xs-pull-10{right:83.33333333%}.col-xs-pull-9{right:75%}.col-xs-pull-8{right:66.66666667%}.col-xs-pull-7{right:58.33333333%}.col-xs-pull-6{right:50%}.col-xs-pull-5{right:41.66666667%}.col-xs-pull-4{right:33.33333333%}.col-xs-pull-3{right:25%}.col-xs-pull-2{right:16.66666667%}.col-xs-pull-1{right:8.33333333%}.col-xs-pull-0{right:auto}.col-xs-push-12{left:100%}.col-xs-push-11{left:91.66666667%}.col-xs-push-10{left:83.33333333%}.col-xs-push-9{left:75%}.col-xs-push-8{left:66.66666667%}.col-xs-push-7{left:58.33333333%}.col-xs-push-6{left:50%}.col-xs-push-5{left:41.66666667%}.col-xs-push-4{left:33.33333333%}.col-xs-push-3{left:25%}.col-xs-push-2{left:16.66666667%}.col-xs-push-1{left:8.33333333%}.col-xs-push-0{left:auto}.col-xs-offset-12{margin-left:100%}.col-xs-offset-11{margin-left:91.66666667%}.col-xs-offset-10{margin-left:83.33333333%}.col-xs-offset-9{margin-left:75%}.col-xs-offset-8{margin-left:66.66666667%}.col-xs-offset-7{margin-left:58.33333333%}.col-xs-offset-6{margin-left:50%}.col-xs-offset-5{margin-left:41.66666667%}.col-xs-offset-4{margin-left:33.33333333%}.col-xs-offset-3{margin-left:25%}.col-xs-offset-2{margin-left:16.66666667%}.col-xs-offset-1{margin-left:8.33333333%}.col-xs-offset-0{margin-left:0}@media (min-width:768px){.col-sm-1,.col-sm-10,.col-sm-11,.col-sm-12,.col-sm-2,.col-sm-3,.col-sm-4,.col-sm-5,.col-sm-6,.col-sm-7,.col-sm-8,.col-sm-9{float:left}.col-sm-12{width:100%}.col-sm-11{width:91.66666667%}.col-sm-10{width:83.33333333%}.col-sm-9{width:75%}.col-sm-8{width:66.66666667%}.col-sm-7{width:58.33333333%}.col-sm-6{width:50%}.col-sm-5{width:41.66666667%}.col-sm-4{width:33.33333333%}.col-sm-3{width:25%}.col-sm-2{width:16.66666667%}.col-sm-1{width:8.33333333%}.col-sm-pull-12{right:100%}.col-sm-pull-11{right:91.66666667%}.col-sm-pull-10{right:83.33333333%}.col-sm-pull-9{right:75%}.col-sm-pull-8{right:66.66666667%}.col-sm-pull-7{right:58.33333333%}.col-sm-pull-6{right:50%}.col-sm-pull-5{right:41.66666667%}.col-sm-pull-4{right:33.33333333%}.col-sm-pull-3{right:25%}.col-sm-pull-2{right:16.66666667%}.col-sm-pull-1{right:8.33333333%}.col-sm-pull-0{right:auto}.col-sm-push-12{left:100%}.col-sm-push-11{left:91.66666667%}.col-sm-push-10{left:83.33333333%}.col-sm-push-9{left:75%}.col-sm-push-8{left:66.66666667%}.col-sm-push-7{left:58.33333333%}.col-sm-push-6{left:50%}.col-sm-push-5{left:41.66666667%}.col-sm-push-4{left:33.33333333%}.col-sm-push-3{left:25%}.col-sm-push-2{left:16.66666667%}.col-sm-push-1{left:8.33333333%}.col-sm-push-0{left:auto}.col-sm-offset-12{margin-left:100%}.col-sm-offset-11{margin-left:91.66666667%}.col-sm-offset-10{margin-left:83.33333333%}.col-sm-offset-9{margin-left:75%}.col-sm-offset-8{margin-left:66.66666667%}.col-sm-offset-7{margin-left:58.33333333%}.col-sm-offset-6{margin-left:50%}.col-sm-offset-5{margin-left:41.66666667%}.col-sm-offset-4{margin-left:33.33333333%}.col-sm-offset-3{margin-left:25%}.col-sm-offset-2{margin-left:16.66666667%}.col-sm-offset-1{margin-left:8.33333333%}.col-sm-offset-0{margin-left:0}}@media (min-width:992px){.col-md-1,.col-md-10,.col-md-11,.col-md-12,.col-md-2,.col-md-3,.col-md-4,.col-md-5,.col-md-6,.col-md-7,.col-md-8,.col-md-9{float:left}.col-md-12{width:100%}.col-md-11{width:91.66666667%}.col-md-10{width:83.33333333%}.col-md-9{width:75%}.col-md-8{width:66.66666667%}.col-md-7{width:58.33333333%}.col-md-6{width:50%}.col-md-5{width:41.66666667%}.col-md-4{width:33.33333333%}.col-md-3{width:25%}.col-md-2{width:16.66666667%}.col-md-1{width:8.33333333%}.col-md-pull-12{right:100%}.col-md-pull-11{right:91.66666667%}.col-md-pull-10{right:83.33333333%}.col-md-pull-9{right:75%}.col-md-pull-8{right:66.66666667%}.col-md-pull-7{right:58.33333333%}.col-md-pull-6{right:50%}.col-md-pull-5{right:41.66666667%}.col-md-pull-4{right:33.33333333%}.col-md-pull-3{right:25%}.col-md-pull-2{right:16.66666667%}.col-md-pull-1{right:8.33333333%}.col-md-pull-0{right:auto}.col-md-push-12{left:100%}.col-md-push-11{left:91.66666667%}.col-md-push-10{left:83.33333333%}.col-md-push-9{left:75%}.col-md-push-8{left:66.66666667%}.col-md-push-7{left:58.33333333%}.col-md-push-6{left:50%}.col-md-push-5{left:41.66666667%}.col-md-push-4{left:33.33333333%}.col-md-push-3{left:25%}.col-md-push-2{left:16.66666667%}.col-md-push-1{left:8.33333333%}.col-md-push-0{left:auto}.col-md-offset-12{margin-left:100%}.col-md-offset-11{margin-left:91.66666667%}.col-md-offset-10{margin-left:83.33333333%}.col-md-offset-9{margin-left:75%}.col-md-offset-8{margin-left:66.66666667%}.col-md-offset-7{margin-left:58.33333333%}.col-md-offset-6{margin-left:50%}.col-md-offset-5{margin-left:41.66666667%}.col-md-offset-4{margin-left:33.33333333%}.col-md-offset-3{margin-left:25%}.col-md-offset-2{margin-left:16.66666667%}.col-md-offset-1{margin-left:8.33333333%}.col-md-offset-0{margin-left:0}}@media (min-width:1200px){.col-lg-1,.col-lg-10,.col-lg-11,.col-lg-12,.col-lg-2,.col-lg-3,.col-lg-4,.col-lg-5,.col-lg-6,.col-lg-7,.col-lg-8,.col-lg-9{float:left}.col-lg-12{width:100%}.col-lg-11{width:91.66666667%}.col-lg-10{width:83.33333333%}.col-lg-9{width:75%}.col-lg-8{width:66.66666667%}.col-lg-7{width:58.33333333%}.col-lg-6{width:50%}.col-lg-5{width:41.66666667%}.col-lg-4{width:33.33333333%}.col-lg-3{width:25%}.col-lg-2{width:16.66666667%}.col-lg-1{width:8.33333333%}.col-lg-pull-12{right:100%}.col-lg-pull-11{right:91.66666667%}.col-lg-pull-10{right:83.33333333%}.col-lg-pull-9{right:75%}.col-lg-pull-8{right:66.66666667%}.col-lg-pull-7{right:58.33333333%}.col-lg-pull-6{right:50%}.col-lg-pull-5{right:41.66666667%}.col-lg-pull-4{right:33.33333333%}.col-lg-pull-3{right:25%}.col-lg-pull-2{right:16.66666667%}.col-lg-pull-1{right:8.33333333%}.col-lg-pull-0{right:auto}.col-lg-push-12{left:100%}.col-lg-push-11{left:91.66666667%}.col-lg-push-10{left:83.33333333%}.col-lg-push-9{left:75%}.col-lg-push-8{left:66.66666667%}.col-lg-push-7{left:58.33333333%}.col-lg-push-6{left:50%}.col-lg-push-5{left:41.66666667%}.col-lg-push-4{left:33.33333333%}.col-lg-push-3{left:25%}.col-lg-push-2{left:16.66666667%}.col-lg-push-1{left:8.33333333%}.col-lg-push-0{left:auto}.col-lg-offset-12{margin-left:100%}.col-lg-offset-11{margin-left:91.66666667%}.col-lg-offset-10{margin-left:83.33333333%}.col-lg-offset-9{margin-left:75%}.col-lg-offset-8{margin-left:66.66666667%}.col-lg-offset-7{margin-left:58.33333333%}.col-lg-offset-6{margin-left:50%}.col-lg-offset-5{margin-left:41.66666667%}.col-lg-offset-4{margin-left:33.33333333%}.col-lg-offset-3{margin-left:25%}.col-lg-offset-2{margin-left:16.66666667%}.col-lg-offset-1{margin-left:8.33333333%}.col-lg-offset-0{margin-left:0}}table{background-color:transparent}caption{padding-top:8px;padding-bottom:8px;color:#777;text-align:left}th{text-align:left}.table{width:100%;max-width:100%;margin-bottom:18px}.table>tbody>tr>td,.table>tbody>tr>th,.table>tfoot>tr>td,.table>tfoot>tr>th,.table>thead>tr>td,.table>thead>tr>th{padding:8px;line-height:1.42857143;vertical-align:top;border-top:1px solid #ddd}.table>thead>tr>th{vertical-align:bottom;border-bottom:2px solid #ddd}.table>caption+thead>tr:first-child>td,.table>caption+thead>tr:first-child>th,.table>colgroup+thead>tr:first-child>td,.table>colgroup+thead>tr:first-child>th,.table>thead:first-child>tr:first-child>td,.table>thead:first-child>tr:first-child>th{border-top:0}.table>tbody+tbody{border-top:2px solid #ddd}.table .table{background-color:#fff}.table-condensed>tbody>tr>td,.table-condensed>tbody>tr>th,.table-condensed>tfoot>tr>td,.table-condensed>tfoot>tr>th,.table-condensed>thead>tr>td,.table-condensed>thead>tr>th{padding:5px}.table-bordered,.table-bordered>tbody>tr>td,.table-bordered>tbody>tr>th,.table-bordered>tfoot>tr>td,.table-bordered>tfoot>tr>th,.table-bordered>thead>tr>td,.table-bordered>thead>tr>th{border:1px solid #ddd}.table-bordered>thead>tr>td,.table-bordered>thead>tr>th{border-bottom-width:2px}.table-striped>tbody>tr:nth-of-type(odd){background-color:#f9f9f9}.table-hover>tbody>tr:hover{background-color:#f5f5f5}table col[class*=col-]{position:static;float:none;display:table-column}table td[class*=col-],table th[class*=col-]{position:static;float:none;display:table-cell}.table>tbody>tr.active>td,.table>tbody>tr.active>th,.table>tbody>tr>td.active,.table>tbody>tr>th.active,.table>tfoot>tr.active>td,.table>tfoot>tr.active>th,.table>tfoot>tr>td.active,.table>tfoot>tr>th.active,.table>thead>tr.active>td,.table>thead>tr.active>th,.table>thead>tr>td.active,.table>thead>tr>th.active{background-color:#f5f5f5}.table-hover>tbody>tr.active:hover>td,.table-hover>tbody>tr.active:hover>th,.table-hover>tbody>tr:hover>.active,.table-hover>tbody>tr>td.active:hover,.table-hover>tbody>tr>th.active:hover{background-color:#e8e8e8}.table>tbody>tr.success>td,.table>tbody>tr.success>th,.table>tbody>tr>td.success,.table>tbody>tr>th.success,.table>tfoot>tr.success>td,.table>tfoot>tr.success>th,.table>tfoot>tr>td.success,.table>tfoot>tr>th.success,.table>thead>tr.success>td,.table>thead>tr.success>th,.table>thead>tr>td.success,.table>thead>tr>th.success{background-color:#dff0d8}.table-hover>tbody>tr.success:hover>td,.table-hover>tbody>tr.success:hover>th,.table-hover>tbody>tr:hover>.success,.table-hover>tbody>tr>td.success:hover,.table-hover>tbody>tr>th.success:hover{background-color:#d0e9c6}.table>tbody>tr.info>td,.table>tbody>tr.info>th,.table>tbody>tr>td.info,.table>tbody>tr>th.info,.table>tfoot>tr.info>td,.table>tfoot>tr.info>th,.table>tfoot>tr>td.info,.table>tfoot>tr>th.info,.table>thead>tr.info>td,.table>thead>tr.info>th,.table>thead>tr>td.info,.table>thead>tr>th.info{background-color:#d9edf7}.table-hover>tbody>tr.info:hover>td,.table-hover>tbody>tr.info:hover>th,.table-hover>tbody>tr:hover>.info,.table-hover>tbody>tr>td.info:hover,.table-hover>tbody>tr>th.info:hover{background-color:#c4e3f3}.table>tbody>tr.warning>td,.table>tbody>tr.warning>th,.table>tbody>tr>td.warning,.table>tbody>tr>th.warning,.table>tfoot>tr.warning>td,.table>tfoot>tr.warning>th,.table>tfoot>tr>td.warning,.table>tfoot>tr>th.warning,.table>thead>tr.warning>td,.table>thead>tr.warning>th,.table>thead>tr>td.warning,.table>thead>tr>th.warning{background-color:#fcf8e3}.table-hover>tbody>tr.warning:hover>td,.table-hover>tbody>tr.warning:hover>th,.table-hover>tbody>tr:hover>.warning,.table-hover>tbody>tr>td.warning:hover,.table-hover>tbody>tr>th.warning:hover{background-color:#faf2cc}.table>tbody>tr.danger>td,.table>tbody>tr.danger>th,.table>tbody>tr>td.danger,.table>tbody>tr>th.danger,.table>tfoot>tr.danger>td,.table>tfoot>tr.danger>th,.table>tfoot>tr>td.danger,.table>tfoot>tr>th.danger,.table>thead>tr.danger>td,.table>thead>tr.danger>th,.table>thead>tr>td.danger,.table>thead>tr>th.danger{background-color:#f2dede}.table-hover>tbody>tr.danger:hover>td,.table-hover>tbody>tr.danger:hover>th,.table-hover>tbody>tr:hover>.danger,.table-hover>tbody>tr>td.danger:hover,.table-hover>tbody>tr>th.danger:hover{background-color:#ebcccc}.table-responsive{overflow-x:auto;min-height:.01%}@media screen and (max-width:767px){.table-responsive{width:100%;margin-bottom:13.5px;overflow-y:hidden;-ms-overflow-style:-ms-autohiding-scrollbar;border:1px solid #ddd}.table-responsive>.table{margin-bottom:0}.table-responsive>.table>tbody>tr>td,.table-responsive>.table>tbody>tr>th,.table-responsive>.table>tfoot>tr>td,.table-responsive>.table>tfoot>tr>th,.table-responsive>.table>thead>tr>td,.table-responsive>.table>thead>tr>th{white-space:nowrap}.table-responsive>.table-bordered{border:0}.table-responsive>.table-bordered>tbody>tr>td:first-child,.table-responsive>.table-bordered>tbody>tr>th:first-child,.table-responsive>.table-bordered>tfoot>tr>td:first-child,.table-responsive>.table-bordered>tfoot>tr>th:first-child,.table-responsive>.table-bordered>thead>tr>td:first-child,.table-responsive>.table-bordered>thead>tr>th:first-child{border-left:0}.table-responsive>.table-bordered>tbody>tr>td:last-child,.table-responsive>.table-bordered>tbody>tr>th:last-child,.table-responsive>.table-bordered>tfoot>tr>td:last-child,.table-responsive>.table-bordered>tfoot>tr>th:last-child,.table-responsive>.table-bordered>thead>tr>td:last-child,.table-responsive>.table-bordered>thead>tr>th:last-child{border-right:0}.table-responsive>.table-bordered>tbody>tr:last-child>td,.table-responsive>.table-bordered>tbody>tr:last-child>th,.table-responsive>.table-bordered>tfoot>tr:last-child>td,.table-responsive>.table-bordered>tfoot>tr:last-child>th{border-bottom:0}}fieldset{padding:0;margin:0;border:0;min-width:0}legend{display:block;width:100%;padding:0;margin-bottom:18px;font-size:19.5px;line-height:inherit;color:#333;border:0;border-bottom:1px solid #e5e5e5}label{display:inline-block;max-width:100%;margin-bottom:5px}input[type=search]{-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box;-webkit-appearance:none}input[type=checkbox],input[type=radio]{margin:4px 0 0;margin-top:1px \9;line-height:normal}input[type=file]{display:block}input[type=range]{display:block;width:100%}select[multiple],select[size]{height:auto}input[type=file]:focus,input[type=checkbox]:focus,input[type=radio]:focus{outline:dotted thin;outline:-webkit-focus-ring-color auto 5px;outline-offset:-2px}output{display:block;padding-top:7px;font-size:13px;line-height:1.42857143;color:#555}.form-control{display:block;width:100%;height:32px;padding:6px 12px;font-size:13px;line-height:1.42857143;color:#555;background-color:#fff;background-image:none;border:1px solid #ccc;border-radius:2px;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.075);box-shadow:inset 0 1px 1px rgba(0,0,0,.075);-webkit-transition:border-color ease-in-out .15s,box-shadow ease-in-out .15s;-o-transition:border-color ease-in-out .15s,box-shadow ease-in-out .15s;transition:border-color ease-in-out .15s,box-shadow ease-in-out .15s}.form-control:focus{border-color:#66afe9;outline:0;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.075),0 0 8px rgba(102,175,233,.6);box-shadow:inset 0 1px 1px rgba(0,0,0,.075),0 0 8px rgba(102,175,233,.6)}.form-control::-moz-placeholder{color:#999;opacity:1}.form-control:-ms-input-placeholder{color:#999}.form-control::-webkit-input-placeholder{color:#999}.form-control[disabled],.form-control[readonly],fieldset[disabled] .form-control{background-color:#eee;opacity:1}.form-control[disabled],fieldset[disabled] .form-control{cursor:not-allowed}textarea.form-control{height:auto}@media screen and (-webkit-min-device-pixel-ratio:0){input[type=date],input[type=time],input[type=datetime-local],input[type=month]{line-height:32px}.input-group-sm input[type=date],.input-group-sm input[type=time],.input-group-sm input[type=datetime-local],.input-group-sm input[type=month],input[type=date].input-sm,input[type=time].input-sm,input[type=datetime-local].input-sm,input[type=month].input-sm{line-height:30px}.input-group-lg input[type=date],.input-group-lg input[type=time],.input-group-lg input[type=datetime-local],.input-group-lg input[type=month],input[type=date].input-lg,input[type=time].input-lg,input[type=datetime-local].input-lg,input[type=month].input-lg{line-height:45px}}.form-group{margin-bottom:15px}.checkbox,.radio{position:relative;display:block;margin-top:10px;margin-bottom:10px}.checkbox label,.radio label{min-height:18px;padding-left:20px;margin-bottom:0;font-weight:400;cursor:pointer}.checkbox input[type=checkbox],.checkbox-inline input[type=checkbox],.radio input[type=radio],.radio-inline input[type=radio]{position:absolute;margin-left:-20px;margin-top:4px \9}.checkbox+.checkbox,.radio+.radio{margin-top:-5px}.checkbox-inline,.radio-inline{position:relative;display:inline-block;padding-left:20px;margin-bottom:0;vertical-align:middle;font-weight:400;cursor:pointer}.checkbox-inline+.checkbox-inline,.radio-inline+.radio-inline{margin-top:0;margin-left:10px}.checkbox-inline.disabled,.checkbox.disabled label,.radio-inline.disabled,.radio.disabled label,fieldset[disabled] .checkbox label,fieldset[disabled] .checkbox-inline,fieldset[disabled] .radio label,fieldset[disabled] .radio-inline,fieldset[disabled] input[type=checkbox],fieldset[disabled] input[type=radio],input[type=checkbox].disabled,input[type=checkbox][disabled],input[type=radio].disabled,input[type=radio][disabled]{cursor:not-allowed}.form-control-static{padding-top:7px;padding-bottom:7px;margin-bottom:0;min-height:31px}.form-control-static.input-lg,.form-control-static.input-sm{padding-left:0;padding-right:0}.input-sm{height:30px;padding:5px 10px;font-size:12px;line-height:1.5;border-radius:1px}select.input-sm{height:30px;line-height:30px}select[multiple].input-sm,textarea.input-sm{height:auto}.form-group-sm .form-control{height:30px;padding:5px 10px;font-size:12px;line-height:1.5;border-radius:1px}select.form-group-sm .form-control{height:30px;line-height:30px}select[multiple].form-group-sm .form-control,textarea.form-group-sm .form-control{height:auto}.form-group-sm .form-control-static{height:30px;padding:5px 10px;font-size:12px;line-height:1.5;min-height:30px}.input-lg{height:45px;padding:10px 16px;font-size:17px;line-height:1.3333333;border-radius:3px}select.input-lg{height:45px;line-height:45px}select[multiple].input-lg,textarea.input-lg{height:auto}.form-group-lg .form-control{height:45px;padding:10px 16px;font-size:17px;line-height:1.3333333;border-radius:3px}select.form-group-lg .form-control{height:45px;line-height:45px}select[multiple].form-group-lg .form-control,textarea.form-group-lg .form-control{height:auto}.form-group-lg .form-control-static{height:45px;padding:10px 16px;font-size:17px;line-height:1.3333333;min-height:35px}.has-feedback{position:relative}.has-feedback .form-control{padding-right:40px}.form-control-feedback{position:absolute;top:0;right:0;z-index:2;display:block;width:32px;height:32px;line-height:32px;text-align:center;pointer-events:none}.input-lg+.form-control-feedback{width:45px;height:45px;line-height:45px}.input-sm+.form-control-feedback{width:30px;height:30px;line-height:30px}.has-success .checkbox,.has-success .checkbox-inline,.has-success .control-label,.has-success .help-block,.has-success .radio,.has-success .radio-inline,.has-success.checkbox label,.has-success.checkbox-inline label,.has-success.radio label,.has-success.radio-inline label{color:#3c763d}.has-success .form-control{border-color:#3c763d;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.075);box-shadow:inset 0 1px 1px rgba(0,0,0,.075)}.has-success .form-control:focus{border-color:#2b542c;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.075),0 0 6px #67b168;box-shadow:inset 0 1px 1px rgba(0,0,0,.075),0 0 6px #67b168}.has-success .input-group-addon{color:#3c763d;border-color:#3c763d;background-color:#dff0d8}.has-success .form-control-feedback{color:#3c763d}.has-warning .checkbox,.has-warning .checkbox-inline,.has-warning .control-label,.has-warning .help-block,.has-warning .radio,.has-warning .radio-inline,.has-warning.checkbox label,.has-warning.checkbox-inline label,.has-warning.radio label,.has-warning.radio-inline label{color:#8a6d3b}.has-warning .form-control{border-color:#8a6d3b;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.075);box-shadow:inset 0 1px 1px rgba(0,0,0,.075)}.has-warning .form-control:focus{border-color:#66512c;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.075),0 0 6px #c0a16b;box-shadow:inset 0 1px 1px rgba(0,0,0,.075),0 0 6px #c0a16b}.has-warning .input-group-addon{color:#8a6d3b;border-color:#8a6d3b;background-color:#fcf8e3}.has-warning .form-control-feedback{color:#8a6d3b}.has-error .checkbox,.has-error .checkbox-inline,.has-error .control-label,.has-error .help-block,.has-error .radio,.has-error .radio-inline,.has-error.checkbox label,.has-error.checkbox-inline label,.has-error.radio label,.has-error.radio-inline label{color:#a94442}.has-error .form-control{border-color:#a94442;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.075);box-shadow:inset 0 1px 1px rgba(0,0,0,.075)}.has-error .form-control:focus{border-color:#843534;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.075),0 0 6px #ce8483;box-shadow:inset 0 1px 1px rgba(0,0,0,.075),0 0 6px #ce8483}.has-error .input-group-addon{color:#a94442;border-color:#a94442;background-color:#f2dede}.has-error .form-control-feedback{color:#a94442}.has-feedback label~.form-control-feedback{top:23px}.has-feedback label.sr-only~.form-control-feedback{top:0}.help-block{display:block;margin-top:5px;margin-bottom:10px;color:#404040}.form-horizontal .checkbox,.form-horizontal .checkbox-inline,.form-horizontal .radio,.form-horizontal .radio-inline{margin-top:0;margin-bottom:0;padding-top:7px}.form-horizontal .checkbox,.form-horizontal .radio{min-height:25px}.form-horizontal .form-group{margin-left:0;margin-right:0}.form-horizontal .has-feedback .form-control-feedback{right:0}@media (min-width:768px){.form-inline .form-group{display:inline-block;margin-bottom:0;vertical-align:middle}.form-inline .form-control{display:inline-block;width:auto;vertical-align:middle}.form-inline .form-control-static{display:inline-block}.form-inline .input-group{display:inline-table;vertical-align:middle}.form-inline .input-group .form-control,.form-inline .input-group .input-group-addon,.form-inline .input-group .input-group-btn{width:auto}.form-inline .input-group>.form-control{width:100%}.form-inline .control-label{margin-bottom:0;vertical-align:middle}.form-inline .checkbox,.form-inline .radio{display:inline-block;margin-top:0;margin-bottom:0;vertical-align:middle}.form-inline .checkbox label,.form-inline .radio label{padding-left:0}.form-inline .checkbox input[type=checkbox],.form-inline .radio input[type=radio]{position:relative;margin-left:0}.form-inline .has-feedback .form-control-feedback{top:0}.form-horizontal .control-label{text-align:right;margin-bottom:0;padding-top:7px}.form-horizontal .form-group-lg .control-label{padding-top:14.33px}.form-horizontal .form-group-sm .control-label{padding-top:6px}}.btn{display:inline-block;margin-bottom:0;font-weight:400;text-align:center;vertical-align:middle;touch-action:manipulation;cursor:pointer;background-image:none;border:1px solid transparent;white-space:nowrap;padding:6px 12px;font-size:13px;line-height:1.42857143;border-radius:2px;-webkit-user-select:none;-moz-user-select:none;-ms-user-select:none;user-select:none}.btn.active.focus,.btn.active:focus,.btn.focus,.btn:active.focus,.btn:active:focus,.btn:focus{outline:dotted thin;outline:-webkit-focus-ring-color auto 5px;outline-offset:-2px}.btn.focus,.btn:focus,.btn:hover{color:#333;text-decoration:none}.btn.active,.btn:active{outline:0;background-image:none;-webkit-box-shadow:inset 0 3px 5px rgba(0,0,0,.125);box-shadow:inset 0 3px 5px rgba(0,0,0,.125)}.btn.disabled,.btn[disabled],fieldset[disabled] .btn{cursor:not-allowed;pointer-events:none;opacity:.65;filter:alpha(opacity=65);-webkit-box-shadow:none;box-shadow:none}.btn-default{color:#333;background-color:#fff;border-color:#ccc}.btn-default.active,.btn-default.focus,.btn-default:active,.btn-default:focus,.btn-default:hover,.open>.dropdown-toggle.btn-default{color:#333;background-color:#e6e6e6;border-color:#adadad}.btn-default.active,.btn-default:active,.open>.dropdown-toggle.btn-default{background-image:none}.btn-default.disabled,.btn-default.disabled.active,.btn-default.disabled.focus,.btn-default.disabled:active,.btn-default.disabled:focus,.btn-default.disabled:hover,.btn-default[disabled],.btn-default[disabled].active,.btn-default[disabled].focus,.btn-default[disabled]:active,.btn-default[disabled]:focus,.btn-default[disabled]:hover,fieldset[disabled] .btn-default,fieldset[disabled] .btn-default.active,fieldset[disabled] .btn-default.focus,fieldset[disabled] .btn-default:active,fieldset[disabled] .btn-default:focus,fieldset[disabled] .btn-default:hover{background-color:#fff;border-color:#ccc}.btn-default .badge{color:#fff;background-color:#333}.btn-primary{color:#fff;background-color:#337ab7;border-color:#2e6da4}.btn-primary.active,.btn-primary.focus,.btn-primary:active,.btn-primary:focus,.btn-primary:hover,.open>.dropdown-toggle.btn-primary{color:#fff;background-color:#286090;border-color:#204d74}.btn-primary.active,.btn-primary:active,.open>.dropdown-toggle.btn-primary{background-image:none}.btn-primary.disabled,.btn-primary.disabled.active,.btn-primary.disabled.focus,.btn-primary.disabled:active,.btn-primary.disabled:focus,.btn-primary.disabled:hover,.btn-primary[disabled],.btn-primary[disabled].active,.btn-primary[disabled].focus,.btn-primary[disabled]:active,.btn-primary[disabled]:focus,.btn-primary[disabled]:hover,fieldset[disabled] .btn-primary,fieldset[disabled] .btn-primary.active,fieldset[disabled] .btn-primary.focus,fieldset[disabled] .btn-primary:active,fieldset[disabled] .btn-primary:focus,fieldset[disabled] .btn-primary:hover{background-color:#337ab7;border-color:#2e6da4}.btn-primary .badge{color:#337ab7;background-color:#fff}.btn-success{color:#fff;background-color:#5cb85c;border-color:#4cae4c}.btn-success.active,.btn-success.focus,.btn-success:active,.btn-success:focus,.btn-success:hover,.open>.dropdown-toggle.btn-success{color:#fff;background-color:#449d44;border-color:#398439}.btn-success.active,.btn-success:active,.open>.dropdown-toggle.btn-success{background-image:none}.btn-success.disabled,.btn-success.disabled.active,.btn-success.disabled.focus,.btn-success.disabled:active,.btn-success.disabled:focus,.btn-success.disabled:hover,.btn-success[disabled],.btn-success[disabled].active,.btn-success[disabled].focus,.btn-success[disabled]:active,.btn-success[disabled]:focus,.btn-success[disabled]:hover,fieldset[disabled] .btn-success,fieldset[disabled] .btn-success.active,fieldset[disabled] .btn-success.focus,fieldset[disabled] .btn-success:active,fieldset[disabled] .btn-success:focus,fieldset[disabled] .btn-success:hover{background-color:#5cb85c;border-color:#4cae4c}.btn-success .badge{color:#5cb85c;background-color:#fff}.btn-info{color:#fff;background-color:#5bc0de;border-color:#46b8da}.btn-info.active,.btn-info.focus,.btn-info:active,.btn-info:focus,.btn-info:hover,.open>.dropdown-toggle.btn-info{color:#fff;background-color:#31b0d5;border-color:#269abc}.btn-info.active,.btn-info:active,.open>.dropdown-toggle.btn-info{background-image:none}.btn-info.disabled,.btn-info.disabled.active,.btn-info.disabled.focus,.btn-info.disabled:active,.btn-info.disabled:focus,.btn-info.disabled:hover,.btn-info[disabled],.btn-info[disabled].active,.btn-info[disabled].focus,.btn-info[disabled]:active,.btn-info[disabled]:focus,.btn-info[disabled]:hover,fieldset[disabled] .btn-info,fieldset[disabled] .btn-info.active,fieldset[disabled] .btn-info.focus,fieldset[disabled] .btn-info:active,fieldset[disabled] .btn-info:focus,fieldset[disabled] .btn-info:hover{background-color:#5bc0de;border-color:#46b8da}.btn-info .badge{color:#5bc0de;background-color:#fff}.btn-warning{color:#fff;background-color:#f0ad4e;border-color:#eea236}.btn-warning.active,.btn-warning.focus,.btn-warning:active,.btn-warning:focus,.btn-warning:hover,.open>.dropdown-toggle.btn-warning{color:#fff;background-color:#ec971f;border-color:#d58512}.btn-warning.active,.btn-warning:active,.open>.dropdown-toggle.btn-warning{background-image:none}.btn-warning.disabled,.btn-warning.disabled.active,.btn-warning.disabled.focus,.btn-warning.disabled:active,.btn-warning.disabled:focus,.btn-warning.disabled:hover,.btn-warning[disabled],.btn-warning[disabled].active,.btn-warning[disabled].focus,.btn-warning[disabled]:active,.btn-warning[disabled]:focus,.btn-warning[disabled]:hover,fieldset[disabled] .btn-warning,fieldset[disabled] .btn-warning.active,fieldset[disabled] .btn-warning.focus,fieldset[disabled] .btn-warning:active,fieldset[disabled] .btn-warning:focus,fieldset[disabled] .btn-warning:hover{background-color:#f0ad4e;border-color:#eea236}.btn-warning .badge{color:#f0ad4e;background-color:#fff}.btn-danger{color:#fff;background-color:#d9534f;border-color:#d43f3a}.btn-danger.active,.btn-danger.focus,.btn-danger:active,.btn-danger:focus,.btn-danger:hover,.open>.dropdown-toggle.btn-danger{color:#fff;background-color:#c9302c;border-color:#ac2925}.btn-danger.active,.btn-danger:active,.open>.dropdown-toggle.btn-danger{background-image:none}.btn-danger.disabled,.btn-danger.disabled.active,.btn-danger.disabled.focus,.btn-danger.disabled:active,.btn-danger.disabled:focus,.btn-danger.disabled:hover,.btn-danger[disabled],.btn-danger[disabled].active,.btn-danger[disabled].focus,.btn-danger[disabled]:active,.btn-danger[disabled]:focus,.btn-danger[disabled]:hover,fieldset[disabled] .btn-danger,fieldset[disabled] .btn-danger.active,fieldset[disabled] .btn-danger.focus,fieldset[disabled] .btn-danger:active,fieldset[disabled] .btn-danger:focus,fieldset[disabled] .btn-danger:hover{background-color:#d9534f;border-color:#d43f3a}.btn-danger .badge{color:#d9534f;background-color:#fff}.btn-link{color:#337ab7;font-weight:400;border-radius:0}.btn-link,.btn-link.active,.btn-link:active,.btn-link[disabled],fieldset[disabled] .btn-link{background-color:transparent;-webkit-box-shadow:none;box-shadow:none}.btn-link,.btn-link:active,.btn-link:focus,.btn-link:hover{border-color:transparent}.btn-link:focus,.btn-link:hover{color:#23527c;text-decoration:underline;background-color:transparent}.btn-link[disabled]:focus,.btn-link[disabled]:hover,fieldset[disabled] .btn-link:focus,fieldset[disabled] .btn-link:hover{color:#777;text-decoration:none}.btn-group-lg>.btn,.btn-lg{padding:10px 16px;font-size:17px;line-height:1.3333333;border-radius:3px}.btn-group-sm>.btn,.btn-sm{padding:5px 10px;font-size:12px;line-height:1.5;border-radius:1px}.btn-group-xs>.btn,.btn-xs{padding:1px 5px;font-size:12px;line-height:1.5;border-radius:1px}.btn-block{display:block;width:100%}.btn-block+.btn-block{margin-top:5px}input[type=button].btn-block,input[type=reset].btn-block,input[type=submit].btn-block{width:100%}.fade{opacity:0;-webkit-transition:opacity .15s linear;-o-transition:opacity .15s linear;transition:opacity .15s linear}.fade.in{opacity:1}.collapse{display:none}.collapse.in{display:block}tr.collapse.in{display:table-row}tbody.collapse.in{display:table-row-group}.collapsing{position:relative;height:0;overflow:hidden;-webkit-transition-property:height,visibility;transition-property:height,visibility;-webkit-transition-duration:.35s;transition-duration:.35s;-webkit-transition-timing-function:ease;transition-timing-function:ease}.caret{display:inline-block;width:0;height:0;margin-left:2px;vertical-align:middle;border-top:4px dashed;border-right:4px solid transparent;border-left:4px solid transparent}.dropdown,.dropup{position:relative}.dropdown-toggle:focus{outline:0}.dropdown-menu{position:absolute;top:100%;left:0;z-index:1000;display:none;float:left;min-width:160px;padding:5px 0;margin:2px 0 0;list-style:none;font-size:13px;text-align:left;background-color:#fff;border:1px solid #ccc;border:1px solid rgba(0,0,0,.15);border-radius:2px;-webkit-box-shadow:0 6px 12px rgba(0,0,0,.175);box-shadow:0 6px 12px rgba(0,0,0,.175);background-clip:padding-box}.dropdown-menu.pull-right{right:0;left:auto}.dropdown-menu .divider{height:1px;margin:8px 0;overflow:hidden;background-color:#e5e5e5}.dropdown-menu>li>a{display:block;padding:3px 20px;clear:both;font-weight:400;line-height:1.42857143;color:#333;white-space:nowrap}.dropdown-menu>li>a:focus,.dropdown-menu>li>a:hover{text-decoration:none;color:#262626;background-color:#f5f5f5}.dropdown-menu>.active>a,.dropdown-menu>.active>a:focus,.dropdown-menu>.active>a:hover{color:#fff;text-decoration:none;outline:0;background-color:#337ab7}.dropdown-menu>.disabled>a,.dropdown-menu>.disabled>a:focus,.dropdown-menu>.disabled>a:hover{color:#777}.dropdown-menu>.disabled>a:focus,.dropdown-menu>.disabled>a:hover{text-decoration:none;background-color:transparent;background-image:none;filter:progid:DXImageTransform.Microsoft.gradient(enabled=false);cursor:not-allowed}.open>.dropdown-menu{display:block}.open>a{outline:0}.dropdown-menu-right{left:auto;right:0}.dropdown-menu-left{left:0;right:auto}.dropdown-header{display:block;padding:3px 20px;font-size:12px;line-height:1.42857143;color:#777;white-space:nowrap}.dropdown-backdrop{position:fixed;left:0;right:0;bottom:0;top:0;z-index:990}.pull-right>.dropdown-menu{right:0;left:auto}.dropup .caret,.navbar-fixed-bottom .dropdown .caret{border-top:0;border-bottom:4px solid;content:""}.dropup .dropdown-menu,.navbar-fixed-bottom .dropdown .dropdown-menu{top:auto;bottom:100%;margin-bottom:2px}@media (min-width:541px){.navbar-right .dropdown-menu{left:auto;right:0}.navbar-right .dropdown-menu-left{left:0;right:auto}}.btn-group,.btn-group-vertical{position:relative;display:inline-block;vertical-align:middle}.btn-group-vertical>.btn,.btn-group>.btn{position:relative;float:left}.btn-group-vertical>.btn.active,.btn-group-vertical>.btn:active,.btn-group-vertical>.btn:focus,.btn-group-vertical>.btn:hover,.btn-group>.btn.active,.btn-group>.btn:active,.btn-group>.btn:focus,.btn-group>.btn:hover{z-index:2}.btn-group .btn+.btn,.btn-group .btn+.btn-group,.btn-group .btn-group+.btn,.btn-group .btn-group+.btn-group{margin-left:-1px}.btn-toolbar{margin-left:-5px}.btn-toolbar .btn-group,.btn-toolbar .input-group{float:left}.btn-toolbar>.btn,.btn-toolbar>.btn-group,.btn-toolbar>.input-group{margin-left:5px}.btn-group>.btn:not(:first-child):not(:last-child):not(.dropdown-toggle){border-radius:0}.btn-group>.btn:first-child{margin-left:0}.btn-group>.btn:first-child:not(:last-child):not(.dropdown-toggle){border-bottom-right-radius:0;border-top-right-radius:0}.btn-group>.btn:last-child:not(:first-child),.btn-group>.dropdown-toggle:not(:first-child){border-bottom-left-radius:0;border-top-left-radius:0}.btn-group>.btn-group{float:left}.btn-group>.btn-group:not(:first-child):not(:last-child)>.btn{border-radius:0}.btn-group>.btn-group:first-child:not(:last-child)>.btn:last-child,.btn-group>.btn-group:first-child:not(:last-child)>.dropdown-toggle{border-bottom-right-radius:0;border-top-right-radius:0}.btn-group>.btn-group:last-child:not(:first-child)>.btn:first-child{border-bottom-left-radius:0;border-top-left-radius:0}.btn-group .dropdown-toggle:active,.btn-group.open .dropdown-toggle{outline:0}.btn-group>.btn+.dropdown-toggle{padding-left:8px;padding-right:8px}.btn-group>.btn-lg+.dropdown-toggle{padding-left:12px;padding-right:12px}.btn-group.open .dropdown-toggle{-webkit-box-shadow:inset 0 3px 5px rgba(0,0,0,.125);box-shadow:inset 0 3px 5px rgba(0,0,0,.125)}.btn-group.open .dropdown-toggle.btn-link{-webkit-box-shadow:none;box-shadow:none}.btn .caret{margin-left:0}.btn-lg .caret{border-width:5px 5px 0}.dropup .btn-lg .caret{border-width:0 5px 5px}.btn-group-vertical>.btn,.btn-group-vertical>.btn-group,.btn-group-vertical>.btn-group>.btn{display:block;float:none;width:100%;max-width:100%}.btn-group-vertical>.btn-group>.btn{float:none}.btn-group-vertical>.btn+.btn,.btn-group-vertical>.btn+.btn-group,.btn-group-vertical>.btn-group+.btn,.btn-group-vertical>.btn-group+.btn-group{margin-top:-1px;margin-left:0}.btn-group-vertical>.btn:not(:first-child):not(:last-child){border-radius:0}.btn-group-vertical>.btn:first-child:not(:last-child){border-top-right-radius:2px;border-bottom-right-radius:0;border-bottom-left-radius:0}.btn-group-vertical>.btn:last-child:not(:first-child){border-bottom-left-radius:2px;border-top-right-radius:0;border-top-left-radius:0}.btn-group-vertical>.btn-group:not(:first-child):not(:last-child)>.btn{border-radius:0}.btn-group-vertical>.btn-group:first-child:not(:last-child)>.btn:last-child,.btn-group-vertical>.btn-group:first-child:not(:last-child)>.dropdown-toggle{border-bottom-right-radius:0;border-bottom-left-radius:0}.btn-group-vertical>.btn-group:last-child:not(:first-child)>.btn:first-child{border-top-right-radius:0;border-top-left-radius:0}.btn-group-justified{display:table;width:100%;table-layout:fixed;border-collapse:separate}.btn-group-justified>.btn,.btn-group-justified>.btn-group{float:none;display:table-cell;width:1%}.btn-group-justified>.btn-group .btn{width:100%}.btn-group-justified>.btn-group .dropdown-menu{left:auto}[data-toggle=buttons]>.btn input[type=checkbox],[data-toggle=buttons]>.btn input[type=radio],[data-toggle=buttons]>.btn-group>.btn input[type=checkbox],[data-toggle=buttons]>.btn-group>.btn input[type=radio]{position:absolute;clip:rect(0,0,0,0);pointer-events:none}.input-group{position:relative;display:table;border-collapse:separate}.input-group[class*=col-]{float:none;padding-left:0;padding-right:0}.input-group .form-control{position:relative;z-index:2;float:left;width:100%;margin-bottom:0}.input-group-lg>.form-control,.input-group-lg>.input-group-addon,.input-group-lg>.input-group-btn>.btn{height:45px;padding:10px 16px;font-size:17px;line-height:1.3333333;border-radius:3px}select.input-group-lg>.form-control,select.input-group-lg>.input-group-addon,select.input-group-lg>.input-group-btn>.btn{height:45px;line-height:45px}select[multiple].input-group-lg>.form-control,select[multiple].input-group-lg>.input-group-addon,select[multiple].input-group-lg>.input-group-btn>.btn,textarea.input-group-lg>.form-control,textarea.input-group-lg>.input-group-addon,textarea.input-group-lg>.input-group-btn>.btn{height:auto}.input-group-sm>.form-control,.input-group-sm>.input-group-addon,.input-group-sm>.input-group-btn>.btn{height:30px;padding:5px 10px;font-size:12px;line-height:1.5;border-radius:1px}select.input-group-sm>.form-control,select.input-group-sm>.input-group-addon,select.input-group-sm>.input-group-btn>.btn{height:30px;line-height:30px}select[multiple].input-group-sm>.form-control,select[multiple].input-group-sm>.input-group-addon,select[multiple].input-group-sm>.input-group-btn>.btn,textarea.input-group-sm>.form-control,textarea.input-group-sm>.input-group-addon,textarea.input-group-sm>.input-group-btn>.btn{height:auto}.input-group .form-control,.input-group-addon,.input-group-btn{display:table-cell}.input-group .form-control:not(:first-child):not(:last-child),.input-group-addon:not(:first-child):not(:last-child),.input-group-btn:not(:first-child):not(:last-child){border-radius:0}.input-group-addon,.input-group-btn{width:1%;white-space:nowrap;vertical-align:middle}.input-group-addon{padding:6px 12px;font-size:13px;font-weight:400;line-height:1;color:#555;text-align:center;background-color:#eee;border:1px solid #ccc;border-radius:2px}.input-group-addon.input-sm{padding:5px 10px;font-size:12px;border-radius:1px}.input-group-addon.input-lg{padding:10px 16px;font-size:17px;border-radius:3px}.input-group-addon input[type=checkbox],.input-group-addon input[type=radio]{margin-top:0}.input-group .form-control:first-child,.input-group-addon:first-child,.input-group-btn:first-child>.btn,.input-group-btn:first-child>.btn-group>.btn,.input-group-btn:first-child>.dropdown-toggle,.input-group-btn:last-child>.btn-group:not(:last-child)>.btn,.input-group-btn:last-child>.btn:not(:last-child):not(.dropdown-toggle){border-bottom-right-radius:0;border-top-right-radius:0}.input-group-addon:first-child{border-right:0}.input-group .form-control:last-child,.input-group-addon:last-child,.input-group-btn:first-child>.btn-group:not(:first-child)>.btn,.input-group-btn:first-child>.btn:not(:first-child),.input-group-btn:last-child>.btn,.input-group-btn:last-child>.btn-group>.btn,.input-group-btn:last-child>.dropdown-toggle{border-bottom-left-radius:0;border-top-left-radius:0}.input-group-addon:last-child{border-left:0}.input-group-btn{position:relative;font-size:0;white-space:nowrap}.input-group-btn>.btn{position:relative}.input-group-btn>.btn+.btn{margin-left:-1px}.input-group-btn>.btn:active,.input-group-btn>.btn:focus,.input-group-btn>.btn:hover{z-index:2}.input-group-btn:first-child>.btn,.input-group-btn:first-child>.btn-group{margin-right:-1px}.input-group-btn:last-child>.btn,.input-group-btn:last-child>.btn-group{margin-left:-1px}.nav{margin-bottom:0;padding-left:0;list-style:none}.nav>li{position:relative;display:block}.nav>li>a{position:relative;display:block;padding:10px 15px}.nav>li>a:focus,.nav>li>a:hover{text-decoration:none;background-color:#eee}.nav>li.disabled>a{color:#777}.nav>li.disabled>a:focus,.nav>li.disabled>a:hover{color:#777;text-decoration:none;background-color:transparent;cursor:not-allowed}.nav .open>a,.nav .open>a:focus,.nav .open>a:hover{background-color:#eee;border-color:#337ab7}.nav .nav-divider{height:1px;margin:8px 0;overflow:hidden;background-color:#e5e5e5}.nav>li>a>img{max-width:none}.nav-tabs{border-bottom:1px solid #ddd}.nav-tabs>li{float:left;margin-bottom:-1px}.nav-tabs>li>a{margin-right:2px;line-height:1.42857143;border:1px solid transparent;border-radius:2px 2px 0 0}.nav-tabs>li>a:hover{border-color:#eee #eee #ddd}.nav-tabs>li.active>a,.nav-tabs>li.active>a:focus,.nav-tabs>li.active>a:hover{color:#555;background-color:#fff;border:1px solid #ddd;border-bottom-color:transparent;cursor:default}.nav-tabs.nav-justified{width:100%;border-bottom:0}.nav-tabs.nav-justified>li{float:none}.nav-tabs.nav-justified>li>a{text-align:center;margin-bottom:5px;margin-right:0;border-radius:2px}.nav-tabs.nav-justified>.dropdown .dropdown-menu{top:auto;left:auto}.nav-tabs.nav-justified>.active>a,.nav-tabs.nav-justified>.active>a:focus,.nav-tabs.nav-justified>.active>a:hover{border:1px solid #ddd}@media (min-width:768px){.nav-tabs.nav-justified>li{display:table-cell;width:1%}.nav-tabs.nav-justified>li>a{margin-bottom:0;border-bottom:1px solid #ddd;border-radius:2px 2px 0 0}.nav-tabs.nav-justified>.active>a,.nav-tabs.nav-justified>.active>a:focus,.nav-tabs.nav-justified>.active>a:hover{border-bottom-color:#fff}}.nav-pills>li{float:left}.nav-pills>li>a{border-radius:2px}.nav-pills>li+li{margin-left:2px}.nav-pills>li.active>a,.nav-pills>li.active>a:focus,.nav-pills>li.active>a:hover{color:#fff;background-color:#337ab7}.nav-stacked>li{float:none}.nav-stacked>li+li{margin-top:2px;margin-left:0}.nav-justified{width:100%}.nav-justified>li{float:none}.nav-justified>li>a{text-align:center;margin-bottom:5px}.nav-justified>.dropdown .dropdown-menu{top:auto;left:auto}.nav-tabs-justified{border-bottom:0}.nav-tabs-justified>li>a{margin-right:0;border-radius:2px}.nav-tabs-justified>.active>a,.nav-tabs-justified>.active>a:focus,.nav-tabs-justified>.active>a:hover{border:1px solid #ddd}@media (min-width:768px){.nav-justified>li{display:table-cell;width:1%}.nav-justified>li>a{margin-bottom:0}.nav-tabs-justified>li>a{border-bottom:1px solid #ddd;border-radius:2px 2px 0 0}.nav-tabs-justified>.active>a,.nav-tabs-justified>.active>a:focus,.nav-tabs-justified>.active>a:hover{border-bottom-color:#fff}}.tab-content>.tab-pane{display:none}.tab-content>.active{display:block}.nav-tabs .dropdown-menu{margin-top:-1px;border-top-right-radius:0;border-top-left-radius:0}.navbar{position:relative;min-height:30px;margin-bottom:18px;border:1px solid transparent}.navbar-collapse{overflow-x:visible;padding-right:0;padding-left:0;border-top:1px solid transparent;box-shadow:inset 0 1px 0 rgba(255,255,255,.1);-webkit-overflow-scrolling:touch}.navbar-collapse.in{overflow-y:auto}.navbar-fixed-bottom .navbar-collapse,.navbar-fixed-top .navbar-collapse{max-height:340px}@media (max-device-width:540px)and (orientation:landscape){.navbar-fixed-bottom .navbar-collapse,.navbar-fixed-top .navbar-collapse{max-height:200px}}.container-fluid>.navbar-collapse,.container-fluid>.navbar-header,.container>.navbar-collapse,.container>.navbar-header{margin-right:0;margin-left:0}.navbar-static-top{z-index:1000;border-width:0 0 1px}.navbar-fixed-bottom,.navbar-fixed-top{position:fixed;right:0;left:0;z-index:1030}@media (min-width:541px){.navbar{border-radius:2px}.navbar-header{float:left}.navbar-collapse{width:auto;border-top:0;box-shadow:none}.navbar-collapse.collapse{display:block!important;height:auto!important;padding-bottom:0;overflow:visible!important}.navbar-collapse.in{overflow-y:visible}.navbar-fixed-bottom .navbar-collapse,.navbar-fixed-top .navbar-collapse,.navbar-static-top .navbar-collapse{padding-left:0;padding-right:0}.container-fluid>.navbar-collapse,.container-fluid>.navbar-header,.container>.navbar-collapse,.container>.navbar-header{margin-right:0;margin-left:0}.navbar-fixed-bottom,.navbar-fixed-top,.navbar-static-top{border-radius:0}}.navbar-fixed-top{top:0;border-width:0 0 1px}.navbar-fixed-bottom{bottom:0;margin-bottom:0;border-width:1px 0 0}.navbar-brand{float:left;padding:6px 0;font-size:17px;line-height:18px;height:30px}.navbar-brand:focus,.navbar-brand:hover{text-decoration:none}.navbar-brand>img{display:block}.navbar-toggle{position:relative;float:right;margin-right:0;padding:9px 10px;margin-top:-2px;margin-bottom:-2px;background-color:transparent;background-image:none;border:1px solid transparent;border-radius:2px}.navbar-toggle:focus{outline:0}.navbar-toggle .icon-bar{display:block;width:22px;height:2px;border-radius:1px}.navbar-toggle .icon-bar+.icon-bar{margin-top:4px}@media (min-width:541px){.navbar>.container .navbar-brand,.navbar>.container-fluid .navbar-brand{margin-left:0}.navbar-toggle{display:none}}.navbar-nav{margin:3px 0}.navbar-nav>li>a{padding-top:10px;padding-bottom:10px;line-height:18px}@media (max-width:540px){.navbar-nav .open .dropdown-menu{position:static;float:none;width:auto;margin-top:0;background-color:transparent;border:0;box-shadow:none}.navbar-nav .open .dropdown-menu .dropdown-header,.navbar-nav .open .dropdown-menu>li>a{padding:5px 15px 5px 25px}.navbar-nav .open .dropdown-menu>li>a{line-height:18px}.navbar-nav .open .dropdown-menu>li>a:focus,.navbar-nav .open .dropdown-menu>li>a:hover{background-image:none}}@media (min-width:541px){.navbar-nav{float:left;margin:0}.navbar-nav>li{float:left}.navbar-nav>li>a{padding-top:6px;padding-bottom:6px}}.navbar-form{padding:10px 0;border-top:1px solid transparent;border-bottom:1px solid transparent;-webkit-box-shadow:inset 0 1px 0 rgba(255,255,255,.1),0 1px 0 rgba(255,255,255,.1);box-shadow:inset 0 1px 0 rgba(255,255,255,.1),0 1px 0 rgba(255,255,255,.1);margin:-1px 0}@media (min-width:768px){.navbar-form .form-group{display:inline-block;margin-bottom:0;vertical-align:middle}.navbar-form .form-control{display:inline-block;width:auto;vertical-align:middle}.navbar-form .form-control-static{display:inline-block}.navbar-form .input-group{display:inline-table;vertical-align:middle}.navbar-form .input-group .form-control,.navbar-form .input-group .input-group-addon,.navbar-form .input-group .input-group-btn{width:auto}.navbar-form .input-group>.form-control{width:100%}.navbar-form .control-label{margin-bottom:0;vertical-align:middle}.navbar-form .checkbox,.navbar-form .radio{display:inline-block;margin-top:0;margin-bottom:0;vertical-align:middle}.navbar-form .checkbox label,.navbar-form .radio label{padding-left:0}.navbar-form .checkbox input[type=checkbox],.navbar-form .radio input[type=radio]{position:relative;margin-left:0}.navbar-form .has-feedback .form-control-feedback{top:0}}@media (max-width:540px){.navbar-form .form-group{margin-bottom:5px}.navbar-form .form-group:last-child{margin-bottom:0}}.navbar-nav>li>.dropdown-menu{margin-top:0;border-top-right-radius:0;border-top-left-radius:0}.navbar-fixed-bottom .navbar-nav>li>.dropdown-menu{margin-bottom:0;border-radius:2px 2px 0 0}.navbar-btn{margin-top:-1px;margin-bottom:-1px}.navbar-btn.btn-sm{margin-top:0;margin-bottom:0}.navbar-btn.btn-xs{margin-top:4px;margin-bottom:4px}.navbar-text{margin-top:6px;margin-bottom:6px}@media (min-width:541px){.navbar-form{width:auto;border:0;margin-left:0;margin-right:0;padding-top:0;padding-bottom:0;-webkit-box-shadow:none;box-shadow:none}.navbar-text{float:left;margin-left:0;margin-right:0}.navbar-left{float:left!important;float:left}.navbar-right{float:right!important;float:right;margin-right:0}.navbar-right~.navbar-right{margin-right:0}}.navbar-default{background-color:#f8f8f8;border-color:#e7e7e7}.navbar-default .navbar-brand{color:#777}.navbar-default .navbar-brand:focus,.navbar-default .navbar-brand:hover{color:#5e5e5e;background-color:transparent}.navbar-default .navbar-nav>li>a,.navbar-default .navbar-text{color:#777}.navbar-default .navbar-nav>li>a:focus,.navbar-default .navbar-nav>li>a:hover{color:#333;background-color:transparent}.navbar-default .navbar-nav>.active>a,.navbar-default .navbar-nav>.active>a:focus,.navbar-default .navbar-nav>.active>a:hover{color:#555;background-color:#e7e7e7}.navbar-default .navbar-nav>.disabled>a,.navbar-default .navbar-nav>.disabled>a:focus,.navbar-default .navbar-nav>.disabled>a:hover{color:#ccc;background-color:transparent}.navbar-default .navbar-toggle{border-color:#ddd}.navbar-default .navbar-toggle:focus,.navbar-default .navbar-toggle:hover{background-color:#ddd}.navbar-default .navbar-toggle .icon-bar{background-color:#888}.navbar-default .navbar-collapse,.navbar-default .navbar-form{border-color:#e7e7e7}.navbar-default .navbar-nav>.open>a,.navbar-default .navbar-nav>.open>a:focus,.navbar-default .navbar-nav>.open>a:hover{background-color:#e7e7e7;color:#555}@media (max-width:540px){.navbar-default .navbar-nav .open .dropdown-menu>li>a{color:#777}.navbar-default .navbar-nav .open .dropdown-menu>li>a:focus,.navbar-default .navbar-nav .open .dropdown-menu>li>a:hover{color:#333;background-color:transparent}.navbar-default .navbar-nav .open .dropdown-menu>.active>a,.navbar-default .navbar-nav .open .dropdown-menu>.active>a:focus,.navbar-default .navbar-nav .open .dropdown-menu>.active>a:hover{color:#555;background-color:#e7e7e7}.navbar-default .navbar-nav .open .dropdown-menu>.disabled>a,.navbar-default .navbar-nav .open .dropdown-menu>.disabled>a:focus,.navbar-default .navbar-nav .open .dropdown-menu>.disabled>a:hover{color:#ccc;background-color:transparent}}.navbar-default .navbar-link{color:#777}.navbar-default .navbar-link:hover{color:#333}.navbar-default .btn-link{color:#777}.navbar-default .btn-link:focus,.navbar-default .btn-link:hover{color:#333}.navbar-default .btn-link[disabled]:focus,.navbar-default .btn-link[disabled]:hover,fieldset[disabled] .navbar-default .btn-link:focus,fieldset[disabled] .navbar-default .btn-link:hover{color:#ccc}.navbar-inverse{background-color:#222;border-color:#080808}.navbar-inverse .navbar-brand{color:#9d9d9d}.navbar-inverse .navbar-brand:focus,.navbar-inverse .navbar-brand:hover{color:#fff;background-color:transparent}.navbar-inverse .navbar-nav>li>a,.navbar-inverse .navbar-text{color:#9d9d9d}.navbar-inverse .navbar-nav>li>a:focus,.navbar-inverse .navbar-nav>li>a:hover{color:#fff;background-color:transparent}.navbar-inverse .navbar-nav>.active>a,.navbar-inverse .navbar-nav>.active>a:focus,.navbar-inverse .navbar-nav>.active>a:hover{color:#fff;background-color:#080808}.navbar-inverse .navbar-nav>.disabled>a,.navbar-inverse .navbar-nav>.disabled>a:focus,.navbar-inverse .navbar-nav>.disabled>a:hover{color:#444;background-color:transparent}.navbar-inverse .navbar-toggle{border-color:#333}.navbar-inverse .navbar-toggle:focus,.navbar-inverse .navbar-toggle:hover{background-color:#333}.navbar-inverse .navbar-toggle .icon-bar{background-color:#fff}.navbar-inverse .navbar-collapse,.navbar-inverse .navbar-form{border-color:#101010}.navbar-inverse .navbar-nav>.open>a,.navbar-inverse .navbar-nav>.open>a:focus,.navbar-inverse .navbar-nav>.open>a:hover{background-color:#080808;color:#fff}@media (max-width:540px){.navbar-inverse .navbar-nav .open .dropdown-menu>.dropdown-header{border-color:#080808}.navbar-inverse .navbar-nav .open .dropdown-menu .divider{background-color:#080808}.navbar-inverse .navbar-nav .open .dropdown-menu>li>a{color:#9d9d9d}.navbar-inverse .navbar-nav .open .dropdown-menu>li>a:focus,.navbar-inverse .navbar-nav .open .dropdown-menu>li>a:hover{color:#fff;background-color:transparent}.navbar-inverse .navbar-nav .open .dropdown-menu>.active>a,.navbar-inverse .navbar-nav .open .dropdown-menu>.active>a:focus,.navbar-inverse .navbar-nav .open .dropdown-menu>.active>a:hover{color:#fff;background-color:#080808}.navbar-inverse .navbar-nav .open .dropdown-menu>.disabled>a,.navbar-inverse .navbar-nav .open .dropdown-menu>.disabled>a:focus,.navbar-inverse .navbar-nav .open .dropdown-menu>.disabled>a:hover{color:#444;background-color:transparent}}.navbar-inverse .navbar-link{color:#9d9d9d}.navbar-inverse .navbar-link:hover{color:#fff}.navbar-inverse .btn-link{color:#9d9d9d}.navbar-inverse .btn-link:focus,.navbar-inverse .btn-link:hover{color:#fff}.navbar-inverse .btn-link[disabled]:focus,.navbar-inverse .btn-link[disabled]:hover,fieldset[disabled] .navbar-inverse .btn-link:focus,fieldset[disabled] .navbar-inverse .btn-link:hover{color:#444}.breadcrumb{padding:8px 15px;margin-bottom:18px;list-style:none;background-color:#f5f5f5;border-radius:2px}.breadcrumb>li{display:inline-block}.breadcrumb>li+li:before{content:"/\00a0";padding:0 5px;color:#5e5e5e}.breadcrumb>.active{color:#777}.pagination{display:inline-block;padding-left:0;margin:18px 0;border-radius:2px}.pagination>li{display:inline}.pagination>li>a,.pagination>li>span{position:relative;float:left;padding:6px 12px;line-height:1.42857143;text-decoration:none;color:#337ab7;background-color:#fff;border:1px solid #ddd;margin-left:-1px}.pagination>li:first-child>a,.pagination>li:first-child>span{margin-left:0;border-bottom-left-radius:2px;border-top-left-radius:2px}.pagination>li:last-child>a,.pagination>li:last-child>span{border-bottom-right-radius:2px;border-top-right-radius:2px}.pagination>li>a:focus,.pagination>li>a:hover,.pagination>li>span:focus,.pagination>li>span:hover{color:#23527c;background-color:#eee;border-color:#ddd}.pagination>.active>a,.pagination>.active>a:focus,.pagination>.active>a:hover,.pagination>.active>span,.pagination>.active>span:focus,.pagination>.active>span:hover{z-index:2;color:#fff;background-color:#337ab7;border-color:#337ab7;cursor:default}.pagination>.disabled>a,.pagination>.disabled>a:focus,.pagination>.disabled>a:hover,.pagination>.disabled>span,.pagination>.disabled>span:focus,.pagination>.disabled>span:hover{color:#777;background-color:#fff;border-color:#ddd;cursor:not-allowed}.pagination-lg>li>a,.pagination-lg>li>span{padding:10px 16px;font-size:17px}.pagination-lg>li:first-child>a,.pagination-lg>li:first-child>span{border-bottom-left-radius:3px;border-top-left-radius:3px}.pagination-lg>li:last-child>a,.pagination-lg>li:last-child>span{border-bottom-right-radius:3px;border-top-right-radius:3px}.pagination-sm>li>a,.pagination-sm>li>span{padding:5px 10px;font-size:12px}.pagination-sm>li:first-child>a,.pagination-sm>li:first-child>span{border-bottom-left-radius:1px;border-top-left-radius:1px}.pagination-sm>li:last-child>a,.pagination-sm>li:last-child>span{border-bottom-right-radius:1px;border-top-right-radius:1px}.pager{padding-left:0;margin:18px 0;list-style:none;text-align:center}.pager li{display:inline}.pager li>a,.pager li>span{display:inline-block;padding:5px 14px;background-color:#fff;border:1px solid #ddd;border-radius:15px}.pager li>a:focus,.pager li>a:hover{text-decoration:none;background-color:#eee}.pager .next>a,.pager .next>span{float:right}.pager .previous>a,.pager .previous>span{float:left}.pager .disabled>a,.pager .disabled>a:focus,.pager .disabled>a:hover,.pager .disabled>span{color:#777;background-color:#fff;cursor:not-allowed}.label{display:inline;padding:.2em .6em .3em;font-size:75%;font-weight:700;line-height:1;color:#fff;text-align:center;white-space:nowrap;vertical-align:baseline;border-radius:.25em}a.label:focus,a.label:hover{color:#fff;text-decoration:none;cursor:pointer}.label:empty{display:none}.btn .label{position:relative;top:-1px}.label-default{background-color:#777}.label-default[href]:focus,.label-default[href]:hover{background-color:#5e5e5e}.label-primary{background-color:#337ab7}.label-primary[href]:focus,.label-primary[href]:hover{background-color:#286090}.label-success{background-color:#5cb85c}.label-success[href]:focus,.label-success[href]:hover{background-color:#449d44}.label-info{background-color:#5bc0de}.label-info[href]:focus,.label-info[href]:hover{background-color:#31b0d5}.label-warning{background-color:#f0ad4e}.label-warning[href]:focus,.label-warning[href]:hover{background-color:#ec971f}.label-danger{background-color:#d9534f}.label-danger[href]:focus,.label-danger[href]:hover{background-color:#c9302c}.badge{display:inline-block;min-width:10px;padding:3px 7px;font-size:12px;font-weight:700;color:#fff;line-height:1;vertical-align:baseline;white-space:nowrap;text-align:center;background-color:#777;border-radius:10px}.badge:empty{display:none}.btn .badge{position:relative;top:-1px}.btn-group-xs>.btn .badge,.btn-xs .badge{top:0;padding:1px 5px}a.badge:focus,a.badge:hover{color:#fff;text-decoration:none;cursor:pointer}.list-group-item.active>.badge,.nav-pills>.active>a>.badge{color:#337ab7;background-color:#fff}.list-group-item>.badge{float:right}.list-group-item>.badge+.badge{margin-right:5px}.nav-pills>li>a>.badge{margin-left:3px}.jumbotron{padding:30px 15px;margin-bottom:30px;color:inherit;background-color:#eee}.jumbotron .h1,.jumbotron h1{color:inherit}.jumbotron p{margin-bottom:15px;font-size:20px;font-weight:200}.jumbotron>hr{border-top-color:#d5d5d5}.container .jumbotron,.container-fluid .jumbotron{border-radius:3px}.jumbotron .container{max-width:100%}@media screen and (min-width:768px){.jumbotron{padding:48px 0}.container .jumbotron,.container-fluid .jumbotron{padding-left:60px;padding-right:60px}.jumbotron .h1,.jumbotron h1{font-size:58.5px}}.thumbnail{display:block;padding:4px;margin-bottom:18px;line-height:1.42857143;background-color:#fff;border:1px solid #ddd;border-radius:2px;-webkit-transition:border .2s ease-in-out;-o-transition:border .2s ease-in-out;transition:border .2s ease-in-out}.thumbnail a>img,.thumbnail>img{margin-left:auto;margin-right:auto}a.thumbnail.active,a.thumbnail:focus,a.thumbnail:hover{border-color:#337ab7}.thumbnail .caption{padding:9px;color:#000}.alert{padding:15px;margin-bottom:18px;border:1px solid transparent;border-radius:2px}.alert h4{margin-top:0;color:inherit}.alert .alert-link{font-weight:700}.alert>p,.alert>ul{margin-bottom:0}.alert>p+p{margin-top:5px}.alert-dismissable,.alert-dismissible{padding-right:35px}.alert-dismissable .close,.alert-dismissible .close{position:relative;top:-2px;right:-21px;color:inherit}.alert-success{background-color:#dff0d8;border-color:#d6e9c6;color:#3c763d}.alert-success hr{border-top-color:#c9e2b3}.alert-success .alert-link{color:#2b542c}.alert-info{background-color:#d9edf7;border-color:#bce8f1;color:#31708f}.alert-info hr{border-top-color:#a6e1ec}.alert-info .alert-link{color:#245269}.alert-warning{background-color:#fcf8e3;border-color:#faebcc;color:#8a6d3b}.alert-warning hr{border-top-color:#f7e1b5}.alert-warning .alert-link{color:#66512c}.alert-danger{background-color:#f2dede;border-color:#ebccd1;color:#a94442}.alert-danger hr{border-top-color:#e4b9c0}.alert-danger .alert-link{color:#843534}@-webkit-keyframes progress-bar-stripes{from{background-position:40px 0}to{background-position:0 0}}@keyframes progress-bar-stripes{from{background-position:40px 0}to{background-position:0 0}}.progress{overflow:hidden;height:18px;margin-bottom:18px;background-color:#f5f5f5;border-radius:2px;-webkit-box-shadow:inset 0 1px 2px rgba(0,0,0,.1);box-shadow:inset 0 1px 2px rgba(0,0,0,.1)}.progress-bar{float:left;width:0;height:100%;font-size:12px;line-height:18px;color:#fff;text-align:center;background-color:#337ab7;-webkit-box-shadow:inset 0 -1px 0 rgba(0,0,0,.15);box-shadow:inset 0 -1px 0 rgba(0,0,0,.15);-webkit-transition:width .6s ease;-o-transition:width .6s ease;transition:width .6s ease}.progress-bar-striped,.progress-striped .progress-bar{background-image:-webkit-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-image:-o-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-image:linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-size:40px 40px}.progress-bar.active,.progress.active .progress-bar{-webkit-animation:progress-bar-stripes 2s linear infinite;-o-animation:progress-bar-stripes 2s linear infinite;animation:progress-bar-stripes 2s linear infinite}.progress-bar-success{background-color:#5cb85c}.progress-striped .progress-bar-success{background-image:-webkit-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-image:-o-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-image:linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent)}.progress-bar-info{background-color:#5bc0de}.progress-striped .progress-bar-info{background-image:-webkit-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-image:-o-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-image:linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent)}.progress-bar-warning{background-color:#f0ad4e}.progress-striped .progress-bar-warning{background-image:-webkit-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-image:-o-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-image:linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent)}.progress-bar-danger{background-color:#d9534f}.progress-striped .progress-bar-danger{background-image:-webkit-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-image:-o-linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent);background-image:linear-gradient(45deg,rgba(255,255,255,.15) 25%,transparent 25%,transparent 50%,rgba(255,255,255,.15) 50%,rgba(255,255,255,.15) 75%,transparent 75%,transparent)}.media{margin-top:15px}.media:first-child{margin-top:0}.media,.media-body{zoom:1;overflow:hidden}.media-body{width:10000px}.media-object{display:block}.media-right,.media>.pull-right{padding-left:10px}.media-left,.media>.pull-left{padding-right:10px}.media-body,.media-left,.media-right{display:table-cell;vertical-align:top}.media-middle{vertical-align:middle}.media-bottom{vertical-align:bottom}.media-heading{margin-top:0;margin-bottom:5px}.media-list{padding-left:0;list-style:none}.list-group{margin-bottom:20px;padding-left:0}.list-group-item{position:relative;display:block;padding:10px 15px;margin-bottom:-1px;background-color:#fff;border:1px solid #ddd}.list-group-item:first-child{border-top-right-radius:2px;border-top-left-radius:2px}.list-group-item:last-child{margin-bottom:0;border-bottom-right-radius:2px;border-bottom-left-radius:2px}a.list-group-item{color:#555}a.list-group-item .list-group-item-heading{color:#333}a.list-group-item:focus,a.list-group-item:hover{text-decoration:none;color:#555;background-color:#f5f5f5}.list-group-item.disabled,.list-group-item.disabled:focus,.list-group-item.disabled:hover{background-color:#eee;color:#777;cursor:not-allowed}.list-group-item.disabled .list-group-item-heading,.list-group-item.disabled:focus .list-group-item-heading,.list-group-item.disabled:hover .list-group-item-heading{color:inherit}.list-group-item.disabled .list-group-item-text,.list-group-item.disabled:focus .list-group-item-text,.list-group-item.disabled:hover .list-group-item-text{color:#777}.list-group-item.active,.list-group-item.active:focus,.list-group-item.active:hover{z-index:2;color:#fff;background-color:#337ab7;border-color:#337ab7}.list-group-item.active .list-group-item-heading,.list-group-item.active .list-group-item-heading>.small,.list-group-item.active .list-group-item-heading>small,.list-group-item.active:focus .list-group-item-heading,.list-group-item.active:focus .list-group-item-heading>.small,.list-group-item.active:focus .list-group-item-heading>small,.list-group-item.active:hover .list-group-item-heading,.list-group-item.active:hover .list-group-item-heading>.small,.list-group-item.active:hover .list-group-item-heading>small{color:inherit}.list-group-item.active .list-group-item-text,.list-group-item.active:focus .list-group-item-text,.list-group-item.active:hover .list-group-item-text{color:#c7ddef}.list-group-item-success{color:#3c763d;background-color:#dff0d8}a.list-group-item-success{color:#3c763d}a.list-group-item-success .list-group-item-heading{color:inherit}a.list-group-item-success:focus,a.list-group-item-success:hover{color:#3c763d;background-color:#d0e9c6}a.list-group-item-success.active,a.list-group-item-success.active:focus,a.list-group-item-success.active:hover{color:#fff;background-color:#3c763d;border-color:#3c763d}.list-group-item-info{color:#31708f;background-color:#d9edf7}a.list-group-item-info{color:#31708f}a.list-group-item-info .list-group-item-heading{color:inherit}a.list-group-item-info:focus,a.list-group-item-info:hover{color:#31708f;background-color:#c4e3f3}a.list-group-item-info.active,a.list-group-item-info.active:focus,a.list-group-item-info.active:hover{color:#fff;background-color:#31708f;border-color:#31708f}.list-group-item-warning{color:#8a6d3b;background-color:#fcf8e3}a.list-group-item-warning{color:#8a6d3b}a.list-group-item-warning .list-group-item-heading{color:inherit}a.list-group-item-warning:focus,a.list-group-item-warning:hover{color:#8a6d3b;background-color:#faf2cc}a.list-group-item-warning.active,a.list-group-item-warning.active:focus,a.list-group-item-warning.active:hover{color:#fff;background-color:#8a6d3b;border-color:#8a6d3b}.list-group-item-danger{color:#a94442;background-color:#f2dede}a.list-group-item-danger{color:#a94442}a.list-group-item-danger .list-group-item-heading{color:inherit}a.list-group-item-danger:focus,a.list-group-item-danger:hover{color:#a94442;background-color:#ebcccc}a.list-group-item-danger.active,a.list-group-item-danger.active:focus,a.list-group-item-danger.active:hover{color:#fff;background-color:#a94442;border-color:#a94442}.list-group-item-heading{margin-top:0;margin-bottom:5px}.list-group-item-text{margin-bottom:0;line-height:1.3}.panel{margin-bottom:18px;background-color:#fff;border:1px solid transparent;border-radius:2px;-webkit-box-shadow:0 1px 1px rgba(0,0,0,.05);box-shadow:0 1px 1px rgba(0,0,0,.05)}.panel-body{padding:15px}.panel-heading{padding:10px 15px;border-bottom:1px solid transparent;border-top-right-radius:1px;border-top-left-radius:1px}.panel-heading>.dropdown .dropdown-toggle{color:inherit}.panel-title{margin-top:0;margin-bottom:0;font-size:15px;color:inherit}.panel-title>.small,.panel-title>.small>a,.panel-title>a,.panel-title>small,.panel-title>small>a{color:inherit}.panel-footer{padding:10px 15px;background-color:#f5f5f5;border-top:1px solid #ddd;border-bottom-right-radius:1px;border-bottom-left-radius:1px}.panel>.list-group,.panel>.panel-collapse>.list-group{margin-bottom:0}.panel>.list-group .list-group-item,.panel>.panel-collapse>.list-group .list-group-item{border-width:1px 0;border-radius:0}.panel>.list-group:first-child .list-group-item:first-child,.panel>.panel-collapse>.list-group:first-child .list-group-item:first-child{border-top:0;border-top-right-radius:1px;border-top-left-radius:1px}.panel>.list-group:last-child .list-group-item:last-child,.panel>.panel-collapse>.list-group:last-child .list-group-item:last-child{border-bottom:0;border-bottom-right-radius:1px;border-bottom-left-radius:1px}.list-group+.panel-footer,.panel-heading+.list-group .list-group-item:first-child{border-top-width:0}.panel>.panel-collapse>.table,.panel>.table,.panel>.table-responsive>.table{margin-bottom:0}.panel>.panel-collapse>.table caption,.panel>.table caption,.panel>.table-responsive>.table caption{padding-left:15px;padding-right:15px}.panel>.table-responsive:first-child>.table:first-child,.panel>.table:first-child{border-top-right-radius:1px;border-top-left-radius:1px}.panel>.table-responsive:first-child>.table:first-child>tbody:first-child>tr:first-child,.panel>.table-responsive:first-child>.table:first-child>thead:first-child>tr:first-child,.panel>.table:first-child>tbody:first-child>tr:first-child,.panel>.table:first-child>thead:first-child>tr:first-child{border-top-left-radius:1px;border-top-right-radius:1px}.panel>.table-responsive:first-child>.table:first-child>tbody:first-child>tr:first-child td:first-child,.panel>.table-responsive:first-child>.table:first-child>tbody:first-child>tr:first-child th:first-child,.panel>.table-responsive:first-child>.table:first-child>thead:first-child>tr:first-child td:first-child,.panel>.table-responsive:first-child>.table:first-child>thead:first-child>tr:first-child th:first-child,.panel>.table:first-child>tbody:first-child>tr:first-child td:first-child,.panel>.table:first-child>tbody:first-child>tr:first-child th:first-child,.panel>.table:first-child>thead:first-child>tr:first-child td:first-child,.panel>.table:first-child>thead:first-child>tr:first-child th:first-child{border-top-left-radius:1px}.panel>.table-responsive:first-child>.table:first-child>tbody:first-child>tr:first-child td:last-child,.panel>.table-responsive:first-child>.table:first-child>tbody:first-child>tr:first-child th:last-child,.panel>.table-responsive:first-child>.table:first-child>thead:first-child>tr:first-child td:last-child,.panel>.table-responsive:first-child>.table:first-child>thead:first-child>tr:first-child th:last-child,.panel>.table:first-child>tbody:first-child>tr:first-child td:last-child,.panel>.table:first-child>tbody:first-child>tr:first-child th:last-child,.panel>.table:first-child>thead:first-child>tr:first-child td:last-child,.panel>.table:first-child>thead:first-child>tr:first-child th:last-child{border-top-right-radius:1px}.panel>.table-responsive:last-child>.table:last-child,.panel>.table:last-child{border-bottom-right-radius:1px;border-bottom-left-radius:1px}.panel>.table-responsive:last-child>.table:last-child>tbody:last-child>tr:last-child,.panel>.table-responsive:last-child>.table:last-child>tfoot:last-child>tr:last-child,.panel>.table:last-child>tbody:last-child>tr:last-child,.panel>.table:last-child>tfoot:last-child>tr:last-child{border-bottom-left-radius:1px;border-bottom-right-radius:1px}.panel>.table-responsive:last-child>.table:last-child>tbody:last-child>tr:last-child td:first-child,.panel>.table-responsive:last-child>.table:last-child>tbody:last-child>tr:last-child th:first-child,.panel>.table-responsive:last-child>.table:last-child>tfoot:last-child>tr:last-child td:first-child,.panel>.table-responsive:last-child>.table:last-child>tfoot:last-child>tr:last-child th:first-child,.panel>.table:last-child>tbody:last-child>tr:last-child td:first-child,.panel>.table:last-child>tbody:last-child>tr:last-child th:first-child,.panel>.table:last-child>tfoot:last-child>tr:last-child td:first-child,.panel>.table:last-child>tfoot:last-child>tr:last-child th:first-child{border-bottom-left-radius:1px}.panel>.table-responsive:last-child>.table:last-child>tbody:last-child>tr:last-child td:last-child,.panel>.table-responsive:last-child>.table:last-child>tbody:last-child>tr:last-child th:last-child,.panel>.table-responsive:last-child>.table:last-child>tfoot:last-child>tr:last-child td:last-child,.panel>.table-responsive:last-child>.table:last-child>tfoot:last-child>tr:last-child th:last-child,.panel>.table:last-child>tbody:last-child>tr:last-child td:last-child,.panel>.table:last-child>tbody:last-child>tr:last-child th:last-child,.panel>.table:last-child>tfoot:last-child>tr:last-child td:last-child,.panel>.table:last-child>tfoot:last-child>tr:last-child th:last-child{border-bottom-right-radius:1px}.panel>.panel-body+.table,.panel>.panel-body+.table-responsive,.panel>.table+.panel-body,.panel>.table-responsive+.panel-body{border-top:1px solid #ddd}.panel>.table>tbody:first-child>tr:first-child td,.panel>.table>tbody:first-child>tr:first-child th{border-top:0}.panel>.table-bordered,.panel>.table-responsive>.table-bordered{border:0}.panel>.table-bordered>tbody>tr>td:first-child,.panel>.table-bordered>tbody>tr>th:first-child,.panel>.table-bordered>tfoot>tr>td:first-child,.panel>.table-bordered>tfoot>tr>th:first-child,.panel>.table-bordered>thead>tr>td:first-child,.panel>.table-bordered>thead>tr>th:first-child,.panel>.table-responsive>.table-bordered>tbody>tr>td:first-child,.panel>.table-responsive>.table-bordered>tbody>tr>th:first-child,.panel>.table-responsive>.table-bordered>tfoot>tr>td:first-child,.panel>.table-responsive>.table-bordered>tfoot>tr>th:first-child,.panel>.table-responsive>.table-bordered>thead>tr>td:first-child,.panel>.table-responsive>.table-bordered>thead>tr>th:first-child{border-left:0}.panel>.table-bordered>tbody>tr>td:last-child,.panel>.table-bordered>tbody>tr>th:last-child,.panel>.table-bordered>tfoot>tr>td:last-child,.panel>.table-bordered>tfoot>tr>th:last-child,.panel>.table-bordered>thead>tr>td:last-child,.panel>.table-bordered>thead>tr>th:last-child,.panel>.table-responsive>.table-bordered>tbody>tr>td:last-child,.panel>.table-responsive>.table-bordered>tbody>tr>th:last-child,.panel>.table-responsive>.table-bordered>tfoot>tr>td:last-child,.panel>.table-responsive>.table-bordered>tfoot>tr>th:last-child,.panel>.table-responsive>.table-bordered>thead>tr>td:last-child,.panel>.table-responsive>.table-bordered>thead>tr>th:last-child{border-right:0}.panel>.table-bordered>tbody>tr:first-child>td,.panel>.table-bordered>tbody>tr:first-child>th,.panel>.table-bordered>tbody>tr:last-child>td,.panel>.table-bordered>tbody>tr:last-child>th,.panel>.table-bordered>tfoot>tr:last-child>td,.panel>.table-bordered>tfoot>tr:last-child>th,.panel>.table-bordered>thead>tr:first-child>td,.panel>.table-bordered>thead>tr:first-child>th,.panel>.table-responsive>.table-bordered>tbody>tr:first-child>td,.panel>.table-responsive>.table-bordered>tbody>tr:first-child>th,.panel>.table-responsive>.table-bordered>tbody>tr:last-child>td,.panel>.table-responsive>.table-bordered>tbody>tr:last-child>th,.panel>.table-responsive>.table-bordered>tfoot>tr:last-child>td,.panel>.table-responsive>.table-bordered>tfoot>tr:last-child>th,.panel>.table-responsive>.table-bordered>thead>tr:first-child>td,.panel>.table-responsive>.table-bordered>thead>tr:first-child>th{border-bottom:0}.panel>.table-responsive{border:0;margin-bottom:0}.panel-group{margin-bottom:18px}.panel-group .panel{margin-bottom:0;border-radius:2px}.panel-group .panel+.panel{margin-top:5px}.panel-group .panel-heading{border-bottom:0}.panel-group .panel-heading+.panel-collapse>.list-group,.panel-group .panel-heading+.panel-collapse>.panel-body{border-top:1px solid #ddd}.panel-group .panel-footer{border-top:0}.panel-group .panel-footer+.panel-collapse .panel-body{border-bottom:1px solid #ddd}.panel-default{border-color:#ddd}.panel-default>.panel-heading{color:#333;background-color:#f5f5f5;border-color:#ddd}.panel-default>.panel-heading+.panel-collapse>.panel-body{border-top-color:#ddd}.panel-default>.panel-heading .badge{color:#f5f5f5;background-color:#333}.panel-default>.panel-footer+.panel-collapse>.panel-body{border-bottom-color:#ddd}.panel-primary{border-color:#337ab7}.panel-primary>.panel-heading{color:#fff;background-color:#337ab7;border-color:#337ab7}.panel-primary>.panel-heading+.panel-collapse>.panel-body{border-top-color:#337ab7}.panel-primary>.panel-heading .badge{color:#337ab7;background-color:#fff}.panel-primary>.panel-footer+.panel-collapse>.panel-body{border-bottom-color:#337ab7}.panel-success{border-color:#d6e9c6}.panel-success>.panel-heading{color:#3c763d;background-color:#dff0d8;border-color:#d6e9c6}.panel-success>.panel-heading+.panel-collapse>.panel-body{border-top-color:#d6e9c6}.panel-success>.panel-heading .badge{color:#dff0d8;background-color:#3c763d}.panel-success>.panel-footer+.panel-collapse>.panel-body{border-bottom-color:#d6e9c6}.panel-info{border-color:#bce8f1}.panel-info>.panel-heading{color:#31708f;background-color:#d9edf7;border-color:#bce8f1}.panel-info>.panel-heading+.panel-collapse>.panel-body{border-top-color:#bce8f1}.panel-info>.panel-heading .badge{color:#d9edf7;background-color:#31708f}.panel-info>.panel-footer+.panel-collapse>.panel-body{border-bottom-color:#bce8f1}.panel-warning{border-color:#faebcc}.panel-warning>.panel-heading{color:#8a6d3b;background-color:#fcf8e3;border-color:#faebcc}.panel-warning>.panel-heading+.panel-collapse>.panel-body{border-top-color:#faebcc}.panel-warning>.panel-heading .badge{color:#fcf8e3;background-color:#8a6d3b}.panel-warning>.panel-footer+.panel-collapse>.panel-body{border-bottom-color:#faebcc}.panel-danger{border-color:#ebccd1}.panel-danger>.panel-heading{color:#a94442;background-color:#f2dede;border-color:#ebccd1}.panel-danger>.panel-heading+.panel-collapse>.panel-body{border-top-color:#ebccd1}.panel-danger>.panel-heading .badge{color:#f2dede;background-color:#a94442}.panel-danger>.panel-footer+.panel-collapse>.panel-body{border-bottom-color:#ebccd1}.embed-responsive{position:relative;display:block;height:0;padding:0;overflow:hidden}.embed-responsive .embed-responsive-item,.embed-responsive embed,.embed-responsive iframe,.embed-responsive object,.embed-responsive video{position:absolute;top:0;left:0;bottom:0;height:100%;width:100%;border:0}.embed-responsive-16by9{padding-bottom:56.25%}.embed-responsive-4by3{padding-bottom:75%}.well{min-height:20px;padding:19px;margin-bottom:20px;background-color:#f5f5f5;border:1px solid #e3e3e3;border-radius:2px;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.05);box-shadow:inset 0 1px 1px rgba(0,0,0,.05)}.well blockquote{border-color:#ddd;border-color:rgba(0,0,0,.15)}.well-lg{padding:24px;border-radius:3px}.well-sm{padding:9px;border-radius:1px}.close{float:right;font-size:19.5px;font-weight:700;line-height:1;color:#000;text-shadow:0 1px 0 #fff;opacity:.2;filter:alpha(opacity=20)}.close:focus,.close:hover{color:#000;text-decoration:none;cursor:pointer;opacity:.5;filter:alpha(opacity=50)}button.close{padding:0;cursor:pointer;background:0 0;border:0;-webkit-appearance:none}.modal-open{overflow:hidden}.modal{display:none;overflow:hidden;position:fixed;top:0;right:0;bottom:0;left:0;z-index:1050;-webkit-overflow-scrolling:touch;outline:0}.modal.fade .modal-dialog{-webkit-transition:-webkit-transform .3s ease-out;-moz-transition:-moz-transform .3s ease-out;-o-transition:-o-transform .3s ease-out;transition:transform .3s ease-out}.modal.in .modal-dialog{-webkit-transform:translate(0,0);-ms-transform:translate(0,0);-o-transform:translate(0,0);transform:translate(0,0)}.modal-open .modal{overflow-x:hidden;overflow-y:auto}.modal-dialog{position:relative;width:auto;margin:10px}.modal-content{position:relative;background-color:#fff;border:1px solid #999;border:1px solid rgba(0,0,0,.2);border-radius:3px;-webkit-box-shadow:0 3px 9px rgba(0,0,0,.5);box-shadow:0 3px 9px rgba(0,0,0,.5);background-clip:padding-box;outline:0}.modal-backdrop{position:fixed;top:0;right:0;bottom:0;left:0;z-index:1040;background-color:#000}.modal-backdrop.fade{opacity:0;filter:alpha(opacity=0)}.modal-backdrop.in{opacity:.5;filter:alpha(opacity=50)}.modal-header{padding:15px;border-bottom:1px solid #e5e5e5;min-height:16.43px}.modal-header .close{margin-top:-2px}.modal-title{margin:0;line-height:1.42857143}.modal-body{position:relative;padding:15px}.modal-footer{padding:15px;text-align:right;border-top:1px solid #e5e5e5}.modal-footer .btn+.btn{margin-left:5px;margin-bottom:0}.modal-footer .btn-group .btn+.btn{margin-left:-1px}.modal-footer .btn-block+.btn-block{margin-left:0}.modal-scrollbar-measure{position:absolute;top:-9999px;width:50px;height:50px;overflow:scroll}@media (min-width:768px){.modal-dialog{width:600px;margin:30px auto}.modal-content{-webkit-box-shadow:0 5px 15px rgba(0,0,0,.5);box-shadow:0 5px 15px rgba(0,0,0,.5)}.modal-sm{width:300px}}@media (min-width:992px){.modal-lg{width:900px}}.tooltip{position:absolute;z-index:1070;display:block;font-family:"Helvetica Neue",Helvetica,Arial,sans-serif;font-size:12px;font-weight:400;line-height:1.4;opacity:0;filter:alpha(opacity=0)}.tooltip.in{opacity:.9;filter:alpha(opacity=90)}.tooltip.top{margin-top:-3px;padding:5px 0}.tooltip.right{margin-left:3px;padding:0 5px}.tooltip.bottom{margin-top:3px;padding:5px 0}.tooltip.left{margin-left:-3px;padding:0 5px}.tooltip-inner{max-width:200px;padding:3px 8px;color:#fff;text-align:center;text-decoration:none;background-color:#000;border-radius:2px}.tooltip-arrow{position:absolute;width:0;height:0;border-color:transparent;border-style:solid}.tooltip.top .tooltip-arrow{bottom:0;left:50%;margin-left:-5px;border-width:5px 5px 0;border-top-color:#000}.tooltip.top-left .tooltip-arrow{bottom:0;right:5px;margin-bottom:-5px;border-width:5px 5px 0;border-top-color:#000}.tooltip.top-right .tooltip-arrow{bottom:0;left:5px;margin-bottom:-5px;border-width:5px 5px 0;border-top-color:#000}.tooltip.right .tooltip-arrow{top:50%;left:0;margin-top:-5px;border-width:5px 5px 5px 0;border-right-color:#000}.tooltip.left .tooltip-arrow{top:50%;right:0;margin-top:-5px;border-width:5px 0 5px 5px;border-left-color:#000}.tooltip.bottom .tooltip-arrow{top:0;left:50%;margin-left:-5px;border-width:0 5px 5px;border-bottom-color:#000}.tooltip.bottom-left .tooltip-arrow{top:0;right:5px;margin-top:-5px;border-width:0 5px 5px;border-bottom-color:#000}.tooltip.bottom-right .tooltip-arrow{top:0;left:5px;margin-top:-5px;border-width:0 5px 5px;border-bottom-color:#000}.popover{position:absolute;top:0;left:0;z-index:1060;display:none;max-width:276px;padding:1px;font-family:"Helvetica Neue",Helvetica,Arial,sans-serif;font-size:13px;font-weight:400;line-height:1.42857143;text-align:left;background-color:#fff;background-clip:padding-box;border:1px solid #ccc;border:1px solid rgba(0,0,0,.2);border-radius:3px;-webkit-box-shadow:0 5px 10px rgba(0,0,0,.2);box-shadow:0 5px 10px rgba(0,0,0,.2);white-space:normal}.popover.top{margin-top:-10px}.popover.right{margin-left:10px}.popover.bottom{margin-top:10px}.popover.left{margin-left:-10px}.popover-title{margin:0;padding:8px 14px;font-size:13px;background-color:#f7f7f7;border-bottom:1px solid #ebebeb;border-radius:2px 2px 0 0}.popover-content{padding:9px 14px}.popover>.arrow,.popover>.arrow:after{position:absolute;display:block;width:0;height:0;border-color:transparent;border-style:solid}.popover>.arrow{border-width:11px}.popover>.arrow:after{border-width:10px;content:""}.popover.top>.arrow{left:50%;margin-left:-11px;border-bottom-width:0;border-top-color:#999;border-top-color:rgba(0,0,0,.25);bottom:-11px}.popover.top>.arrow:after{content:" ";bottom:1px;margin-left:-10px;border-bottom-width:0;border-top-color:#fff}.popover.right>.arrow{top:50%;left:-11px;margin-top:-11px;border-left-width:0;border-right-color:#999;border-right-color:rgba(0,0,0,.25)}.popover.right>.arrow:after{content:" ";left:1px;bottom:-10px;border-left-width:0;border-right-color:#fff}.popover.bottom>.arrow{left:50%;margin-left:-11px;border-top-width:0;border-bottom-color:#999;border-bottom-color:rgba(0,0,0,.25);top:-11px}.popover.bottom>.arrow:after{content:" ";top:1px;margin-left:-10px;border-top-width:0;border-bottom-color:#fff}.popover.left>.arrow{top:50%;right:-11px;margin-top:-11px;border-right-width:0;border-left-color:#999;border-left-color:rgba(0,0,0,.25)}.popover.left>.arrow:after{content:" ";right:1px;border-right-width:0;border-left-color:#fff;bottom:-10px}.carousel{position:relative}.carousel-inner{position:relative;overflow:hidden;width:100%}.carousel-inner>.item{display:none;position:relative;-webkit-transition:.6s ease-in-out left;-o-transition:.6s ease-in-out left;transition:.6s ease-in-out left}.carousel-inner>.item>a>img,.carousel-inner>.item>img{line-height:1}@media all and (transform-3d),(-webkit-transform-3d){.carousel-inner>.item{-webkit-transition:-webkit-transform .6s ease-in-out;-moz-transition:-moz-transform .6s ease-in-out;-o-transition:-o-transform .6s ease-in-out;transition:transform .6s ease-in-out;-webkit-backface-visibility:hidden;-moz-backface-visibility:hidden;backface-visibility:hidden;-webkit-perspective:1000;-moz-perspective:1000;perspective:1000}.carousel-inner>.item.active.right,.carousel-inner>.item.next{-webkit-transform:translate3d(100%,0,0);transform:translate3d(100%,0,0);left:0}.carousel-inner>.item.active.left,.carousel-inner>.item.prev{-webkit-transform:translate3d(-100%,0,0);transform:translate3d(-100%,0,0);left:0}.carousel-inner>.item.active,.carousel-inner>.item.next.left,.carousel-inner>.item.prev.right{-webkit-transform:translate3d(0,0,0);transform:translate3d(0,0,0);left:0}}.carousel-inner>.active,.carousel-inner>.next,.carousel-inner>.prev{display:block}.carousel-inner>.active{left:0}.carousel-inner>.next,.carousel-inner>.prev{position:absolute;top:0;width:100%}.carousel-inner>.next{left:100%}.carousel-inner>.prev{left:-100%}.carousel-inner>.next.left,.carousel-inner>.prev.right{left:0}.carousel-inner>.active.left{left:-100%}.carousel-inner>.active.right{left:100%}.carousel-control{position:absolute;top:0;left:0;bottom:0;width:15%;opacity:.5;filter:alpha(opacity=50);font-size:20px;color:#fff;text-align:center;text-shadow:0 1px 2px rgba(0,0,0,.6)}.carousel-control.left{background-image:-webkit-linear-gradient(left,rgba(0,0,0,.5) 0,rgba(0,0,0,.0001) 100%);background-image:-o-linear-gradient(left,rgba(0,0,0,.5) 0,rgba(0,0,0,.0001) 100%);background-image:linear-gradient(to right,rgba(0,0,0,.5) 0,rgba(0,0,0,.0001) 100%);background-repeat:repeat-x;filter:progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1)}.carousel-control.right{left:auto;right:0;background-image:-webkit-linear-gradient(left,rgba(0,0,0,.0001) 0,rgba(0,0,0,.5) 100%);background-image:-o-linear-gradient(left,rgba(0,0,0,.0001) 0,rgba(0,0,0,.5) 100%);background-image:linear-gradient(to right,rgba(0,0,0,.0001) 0,rgba(0,0,0,.5) 100%);background-repeat:repeat-x;filter:progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1)}.carousel-control:focus,.carousel-control:hover{outline:0;color:#fff;text-decoration:none;opacity:.9;filter:alpha(opacity=90)}.carousel-control .glyphicon-chevron-left,.carousel-control .glyphicon-chevron-right,.carousel-control .icon-next,.carousel-control .icon-prev{position:absolute;top:50%;z-index:5;display:inline-block}.carousel-control .glyphicon-chevron-left,.carousel-control .icon-prev{left:50%;margin-left:-10px}.carousel-control .glyphicon-chevron-right,.carousel-control .icon-next{right:50%;margin-right:-10px}.carousel-control .icon-next,.carousel-control .icon-prev{width:20px;height:20px;margin-top:-10px;line-height:1;font-family:serif}.carousel-control .icon-prev:before{content:'\2039'}.carousel-control .icon-next:before{content:'\203a'}.carousel-indicators{position:absolute;bottom:10px;left:50%;z-index:15;width:60%;margin-left:-30%;padding-left:0;list-style:none;text-align:center}.carousel-indicators li{display:inline-block;width:10px;height:10px;margin:1px;text-indent:-999px;border:1px solid #fff;border-radius:10px;cursor:pointer;background-color:transparent}.carousel-indicators .active{margin:0;width:12px;height:12px;background-color:#fff}.carousel-caption{position:absolute;left:15%;right:15%;bottom:20px;z-index:10;padding-top:20px;padding-bottom:20px;color:#fff;text-align:center;text-shadow:0 1px 2px rgba(0,0,0,.6)}.carousel-caption .btn{text-shadow:none}@media screen and (min-width:768px){.carousel-control .glyphicon-chevron-left,.carousel-control .glyphicon-chevron-right,.carousel-control .icon-next,.carousel-control .icon-prev{width:30px;height:30px;margin-top:-15px;font-size:30px}.carousel-control .glyphicon-chevron-left,.carousel-control .icon-prev{margin-left:-15px}.carousel-control .glyphicon-chevron-right,.carousel-control .icon-next{margin-right:-15px}.carousel-caption{left:20%;right:20%;padding-bottom:30px}.carousel-indicators{bottom:20px}}.btn-group-vertical>.btn-group:after,.btn-group-vertical>.btn-group:before,.btn-toolbar:after,.btn-toolbar:before,.clearfix:after,.clearfix:before,.container-fluid:after,.container-fluid:before,.container:after,.container:before,.dl-horizontal dd:after,.dl-horizontal dd:before,.form-horizontal .form-group:after,.form-horizontal .form-group:before,.item_buttons:after,.item_buttons:before,.modal-footer:after,.modal-footer:before,.nav:after,.nav:before,.navbar-collapse:after,.navbar-collapse:before,.navbar-header:after,.navbar-header:before,.navbar:after,.navbar:before,.pager:after,.pager:before,.panel-body:after,.panel-body:before,.row:after,.row:before{content:" ";display:table}.btn-group-vertical>.btn-group:after,.btn-toolbar:after,.clearfix:after,.container-fluid:after,.container:after,.dl-horizontal dd:after,.form-horizontal .form-group:after,.item_buttons:after,.modal-footer:after,.nav:after,.navbar-collapse:after,.navbar-header:after,.navbar:after,.pager:after,.panel-body:after,.row:after{clear:both}.center-block{display:block;margin-left:auto;margin-right:auto}.pull-right{float:right!important}.pull-left{float:left!important}.hide{display:none!important}.show{display:block!important}.invisible{visibility:hidden}.text-hide{font:0/0 a;color:transparent;text-shadow:none;background-color:transparent;border:0}.hidden{display:none!important}.affix{position:fixed}@-ms-viewport{width:device-width}.visible-lg,.visible-lg-block,.visible-lg-inline,.visible-lg-inline-block,.visible-md,.visible-md-block,.visible-md-inline,.visible-md-inline-block,.visible-sm,.visible-sm-block,.visible-sm-inline,.visible-sm-inline-block,.visible-xs,.visible-xs-block,.visible-xs-inline,.visible-xs-inline-block{display:none!important}@media (max-width:767px){.visible-xs{display:block!important}table.visible-xs{display:table}tr.visible-xs{display:table-row!important}td.visible-xs,th.visible-xs{display:table-cell!important}.visible-xs-block{display:block!important}.visible-xs-inline{display:inline!important}.visible-xs-inline-block{display:inline-block!important}}@media (min-width:768px)and (max-width:991px){.visible-sm{display:block!important}table.visible-sm{display:table}tr.visible-sm{display:table-row!important}td.visible-sm,th.visible-sm{display:table-cell!important}.visible-sm-block{display:block!important}.visible-sm-inline{display:inline!important}.visible-sm-inline-block{display:inline-block!important}}@media (min-width:992px)and (max-width:1199px){.visible-md{display:block!important}table.visible-md{display:table}tr.visible-md{display:table-row!important}td.visible-md,th.visible-md{display:table-cell!important}.visible-md-block{display:block!important}.visible-md-inline{display:inline!important}.visible-md-inline-block{display:inline-block!important}}@media (min-width:1200px){.visible-lg{display:block!important}table.visible-lg{display:table}tr.visible-lg{display:table-row!important}td.visible-lg,th.visible-lg{display:table-cell!important}.visible-lg-block{display:block!important}.visible-lg-inline{display:inline!important}.visible-lg-inline-block{display:inline-block!important}}@media (max-width:767px){.hidden-xs{display:none!important}}@media (min-width:768px)and (max-width:991px){.hidden-sm{display:none!important}}@media (min-width:992px)and (max-width:1199px){.hidden-md{display:none!important}}@media (min-width:1200px){.hidden-lg{display:none!important}}.visible-print{display:none!important}@media print{.visible-print{display:block!important}table.visible-print{display:table}tr.visible-print{display:table-row!important}td.visible-print,th.visible-print{display:table-cell!important}}.visible-print-block{display:none!important}@media print{.visible-print-block{display:block!important}}.visible-print-inline{display:none!important}@media print{.visible-print-inline{display:inline!important}}.visible-print-inline-block{display:none!important}@media print{.visible-print-inline-block{display:inline-block!important}.hidden-print{display:none!important}}/*!
*
* Font Awesome
*
*//*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */@font-face{font-family:'FontAwesome';src:url(../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0);src:url(../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0)format('embedded-opentype'),url(../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0)format('woff'),url(../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0)format('truetype'),url(../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular)format('svg');font-weight:400;font-style:normal}.fa{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale}.fa-lg{font-size:1.33333333em;line-height:.75em;vertical-align:-15%}.fa-2x{font-size:2em}.fa-3x{font-size:3em}.fa-4x{font-size:4em}.fa-5x{font-size:5em}.fa-fw{width:1.28571429em;text-align:center}.fa-ul{padding-left:0;margin-left:2.14285714em;list-style-type:none}.fa-ul>li{position:relative}.fa-li{position:absolute;left:-2.14285714em;width:2.14285714em;top:.14285714em;text-align:center}.fa-li.fa-lg{left:-1.85714286em}.fa-border{padding:.2em .25em .15em;border:.08em solid #eee;border-radius:.1em}.fa.pull-left{margin-right:.3em}.fa.pull-right{margin-left:.3em}.fa-spin{-webkit-animation:fa-spin 2s infinite linear;animation:fa-spin 2s infinite linear}@-webkit-keyframes fa-spin{0%{-webkit-transform:rotate(0);transform:rotate(0)}100%{-webkit-transform:rotate(359deg);transform:rotate(359deg)}}@keyframes fa-spin{0%{-webkit-transform:rotate(0);transform:rotate(0)}100%{-webkit-transform:rotate(359deg);transform:rotate(359deg)}}.fa-rotate-90{filter:progid:DXImageTransform.Microsoft.BasicImage(rotation=1);-webkit-transform:rotate(90deg);-ms-transform:rotate(90deg);transform:rotate(90deg)}.fa-rotate-180{filter:progid:DXImageTransform.Microsoft.BasicImage(rotation=2);-webkit-transform:rotate(180deg);-ms-transform:rotate(180deg);transform:rotate(180deg)}.fa-rotate-270{filter:progid:DXImageTransform.Microsoft.BasicImage(rotation=3);-webkit-transform:rotate(270deg);-ms-transform:rotate(270deg);transform:rotate(270deg)}.fa-flip-horizontal{filter:progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);-webkit-transform:scale(-1,1);-ms-transform:scale(-1,1);transform:scale(-1,1)}.fa-flip-vertical{filter:progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);-webkit-transform:scale(1,-1);-ms-transform:scale(1,-1);transform:scale(1,-1)}:root .fa-flip-horizontal,:root .fa-flip-vertical,:root .fa-rotate-180,:root .fa-rotate-270,:root .fa-rotate-90{filter:none}.fa-stack{position:relative;display:inline-block;width:2em;height:2em;line-height:2em;vertical-align:middle}.fa-stack-1x,.fa-stack-2x{position:absolute;left:0;width:100%;text-align:center}.fa-stack-1x{line-height:inherit}.fa-stack-2x{font-size:2em}.fa-inverse{color:#fff}.fa-glass:before{content:"\f000"}.fa-music:before{content:"\f001"}.fa-search:before{content:"\f002"}.fa-envelope-o:before{content:"\f003"}.fa-heart:before{content:"\f004"}.fa-star:before{content:"\f005"}.fa-star-o:before{content:"\f006"}.fa-user:before{content:"\f007"}.fa-film:before{content:"\f008"}.fa-th-large:before{content:"\f009"}.fa-th:before{content:"\f00a"}.fa-th-list:before{content:"\f00b"}.fa-check:before{content:"\f00c"}.fa-close:before,.fa-remove:before,.fa-times:before{content:"\f00d"}.fa-search-plus:before{content:"\f00e"}.fa-search-minus:before{content:"\f010"}.fa-power-off:before{content:"\f011"}.fa-signal:before{content:"\f012"}.fa-cog:before,.fa-gear:before{content:"\f013"}.fa-trash-o:before{content:"\f014"}.fa-home:before{content:"\f015"}.fa-file-o:before{content:"\f016"}.fa-clock-o:before{content:"\f017"}.fa-road:before{content:"\f018"}.fa-download:before{content:"\f019"}.fa-arrow-circle-o-down:before{content:"\f01a"}.fa-arrow-circle-o-up:before{content:"\f01b"}.fa-inbox:before{content:"\f01c"}.fa-play-circle-o:before{content:"\f01d"}.fa-repeat:before,.fa-rotate-right:before{content:"\f01e"}.fa-refresh:before{content:"\f021"}.fa-list-alt:before{content:"\f022"}.fa-lock:before{content:"\f023"}.fa-flag:before{content:"\f024"}.fa-headphones:before{content:"\f025"}.fa-volume-off:before{content:"\f026"}.fa-volume-down:before{content:"\f027"}.fa-volume-up:before{content:"\f028"}.fa-qrcode:before{content:"\f029"}.fa-barcode:before{content:"\f02a"}.fa-tag:before{content:"\f02b"}.fa-tags:before{content:"\f02c"}.fa-book:before{content:"\f02d"}.fa-bookmark:before{content:"\f02e"}.fa-print:before{content:"\f02f"}.fa-camera:before{content:"\f030"}.fa-font:before{content:"\f031"}.fa-bold:before{content:"\f032"}.fa-italic:before{content:"\f033"}.fa-text-height:before{content:"\f034"}.fa-text-width:before{content:"\f035"}.fa-align-left:before{content:"\f036"}.fa-align-center:before{content:"\f037"}.fa-align-right:before{content:"\f038"}.fa-align-justify:before{content:"\f039"}.fa-list:before{content:"\f03a"}.fa-dedent:before,.fa-outdent:before{content:"\f03b"}.fa-indent:before{content:"\f03c"}.fa-video-camera:before{content:"\f03d"}.fa-image:before,.fa-photo:before,.fa-picture-o:before{content:"\f03e"}.fa-pencil:before{content:"\f040"}.fa-map-marker:before{content:"\f041"}.fa-adjust:before{content:"\f042"}.fa-tint:before{content:"\f043"}.fa-edit:before,.fa-pencil-square-o:before{content:"\f044"}.fa-share-square-o:before{content:"\f045"}.fa-check-square-o:before{content:"\f046"}.fa-arrows:before{content:"\f047"}.fa-step-backward:before{content:"\f048"}.fa-fast-backward:before{content:"\f049"}.fa-backward:before{content:"\f04a"}.fa-play:before{content:"\f04b"}.fa-pause:before{content:"\f04c"}.fa-stop:before{content:"\f04d"}.fa-forward:before{content:"\f04e"}.fa-fast-forward:before{content:"\f050"}.fa-step-forward:before{content:"\f051"}.fa-eject:before{content:"\f052"}.fa-chevron-left:before{content:"\f053"}.fa-chevron-right:before{content:"\f054"}.fa-plus-circle:before{content:"\f055"}.fa-minus-circle:before{content:"\f056"}.fa-times-circle:before{content:"\f057"}.fa-check-circle:before{content:"\f058"}.fa-question-circle:before{content:"\f059"}.fa-info-circle:before{content:"\f05a"}.fa-crosshairs:before{content:"\f05b"}.fa-times-circle-o:before{content:"\f05c"}.fa-check-circle-o:before{content:"\f05d"}.fa-ban:before{content:"\f05e"}.fa-arrow-left:before{content:"\f060"}.fa-arrow-right:before{content:"\f061"}.fa-arrow-up:before{content:"\f062"}.fa-arrow-down:before{content:"\f063"}.fa-mail-forward:before,.fa-share:before{content:"\f064"}.fa-expand:before{content:"\f065"}.fa-compress:before{content:"\f066"}.fa-plus:before{content:"\f067"}.fa-minus:before{content:"\f068"}.fa-asterisk:before{content:"\f069"}.fa-exclamation-circle:before{content:"\f06a"}.fa-gift:before{content:"\f06b"}.fa-leaf:before{content:"\f06c"}.fa-fire:before{content:"\f06d"}.fa-eye:before{content:"\f06e"}.fa-eye-slash:before{content:"\f070"}.fa-exclamation-triangle:before,.fa-warning:before{content:"\f071"}.fa-plane:before{content:"\f072"}.fa-calendar:before{content:"\f073"}.fa-random:before{content:"\f074"}.fa-comment:before{content:"\f075"}.fa-magnet:before{content:"\f076"}.fa-chevron-up:before{content:"\f077"}.fa-chevron-down:before{content:"\f078"}.fa-retweet:before{content:"\f079"}.fa-shopping-cart:before{content:"\f07a"}.fa-folder:before{content:"\f07b"}.fa-folder-open:before{content:"\f07c"}.fa-arrows-v:before{content:"\f07d"}.fa-arrows-h:before{content:"\f07e"}.fa-bar-chart-o:before,.fa-bar-chart:before{content:"\f080"}.fa-twitter-square:before{content:"\f081"}.fa-facebook-square:before{content:"\f082"}.fa-camera-retro:before{content:"\f083"}.fa-key:before{content:"\f084"}.fa-cogs:before,.fa-gears:before{content:"\f085"}.fa-comments:before{content:"\f086"}.fa-thumbs-o-up:before{content:"\f087"}.fa-thumbs-o-down:before{content:"\f088"}.fa-star-half:before{content:"\f089"}.fa-heart-o:before{content:"\f08a"}.fa-sign-out:before{content:"\f08b"}.fa-linkedin-square:before{content:"\f08c"}.fa-thumb-tack:before{content:"\f08d"}.fa-external-link:before{content:"\f08e"}.fa-sign-in:before{content:"\f090"}.fa-trophy:before{content:"\f091"}.fa-github-square:before{content:"\f092"}.fa-upload:before{content:"\f093"}.fa-lemon-o:before{content:"\f094"}.fa-phone:before{content:"\f095"}.fa-square-o:before{content:"\f096"}.fa-bookmark-o:before{content:"\f097"}.fa-phone-square:before{content:"\f098"}.fa-twitter:before{content:"\f099"}.fa-facebook:before{content:"\f09a"}.fa-github:before{content:"\f09b"}.fa-unlock:before{content:"\f09c"}.fa-credit-card:before{content:"\f09d"}.fa-rss:before{content:"\f09e"}.fa-hdd-o:before{content:"\f0a0"}.fa-bullhorn:before{content:"\f0a1"}.fa-bell:before{content:"\f0f3"}.fa-certificate:before{content:"\f0a3"}.fa-hand-o-right:before{content:"\f0a4"}.fa-hand-o-left:before{content:"\f0a5"}.fa-hand-o-up:before{content:"\f0a6"}.fa-hand-o-down:before{content:"\f0a7"}.fa-arrow-circle-left:before{content:"\f0a8"}.fa-arrow-circle-right:before{content:"\f0a9"}.fa-arrow-circle-up:before{content:"\f0aa"}.fa-arrow-circle-down:before{content:"\f0ab"}.fa-globe:before{content:"\f0ac"}.fa-wrench:before{content:"\f0ad"}.fa-tasks:before{content:"\f0ae"}.fa-filter:before{content:"\f0b0"}.fa-briefcase:before{content:"\f0b1"}.fa-arrows-alt:before{content:"\f0b2"}.fa-group:before,.fa-users:before{content:"\f0c0"}.fa-chain:before,.fa-link:before{content:"\f0c1"}.fa-cloud:before{content:"\f0c2"}.fa-flask:before{content:"\f0c3"}.fa-cut:before,.fa-scissors:before{content:"\f0c4"}.fa-copy:before,.fa-files-o:before{content:"\f0c5"}.fa-paperclip:before{content:"\f0c6"}.fa-floppy-o:before,.fa-save:before{content:"\f0c7"}.fa-square:before{content:"\f0c8"}.fa-bars:before,.fa-navicon:before,.fa-reorder:before{content:"\f0c9"}.fa-list-ul:before{content:"\f0ca"}.fa-list-ol:before{content:"\f0cb"}.fa-strikethrough:before{content:"\f0cc"}.fa-underline:before{content:"\f0cd"}.fa-table:before{content:"\f0ce"}.fa-magic:before{content:"\f0d0"}.fa-truck:before{content:"\f0d1"}.fa-pinterest:before{content:"\f0d2"}.fa-pinterest-square:before{content:"\f0d3"}.fa-google-plus-square:before{content:"\f0d4"}.fa-google-plus:before{content:"\f0d5"}.fa-money:before{content:"\f0d6"}.fa-caret-down:before{content:"\f0d7"}.fa-caret-up:before{content:"\f0d8"}.fa-caret-left:before{content:"\f0d9"}.fa-caret-right:before{content:"\f0da"}.fa-columns:before{content:"\f0db"}.fa-sort:before,.fa-unsorted:before{content:"\f0dc"}.fa-sort-desc:before,.fa-sort-down:before{content:"\f0dd"}.fa-sort-asc:before,.fa-sort-up:before{content:"\f0de"}.fa-envelope:before{content:"\f0e0"}.fa-linkedin:before{content:"\f0e1"}.fa-rotate-left:before,.fa-undo:before{content:"\f0e2"}.fa-gavel:before,.fa-legal:before{content:"\f0e3"}.fa-dashboard:before,.fa-tachometer:before{content:"\f0e4"}.fa-comment-o:before{content:"\f0e5"}.fa-comments-o:before{content:"\f0e6"}.fa-bolt:before,.fa-flash:before{content:"\f0e7"}.fa-sitemap:before{content:"\f0e8"}.fa-umbrella:before{content:"\f0e9"}.fa-clipboard:before,.fa-paste:before{content:"\f0ea"}.fa-lightbulb-o:before{content:"\f0eb"}.fa-exchange:before{content:"\f0ec"}.fa-cloud-download:before{content:"\f0ed"}.fa-cloud-upload:before{content:"\f0ee"}.fa-user-md:before{content:"\f0f0"}.fa-stethoscope:before{content:"\f0f1"}.fa-suitcase:before{content:"\f0f2"}.fa-bell-o:before{content:"\f0a2"}.fa-coffee:before{content:"\f0f4"}.fa-cutlery:before{content:"\f0f5"}.fa-file-text-o:before{content:"\f0f6"}.fa-building-o:before{content:"\f0f7"}.fa-hospital-o:before{content:"\f0f8"}.fa-ambulance:before{content:"\f0f9"}.fa-medkit:before{content:"\f0fa"}.fa-fighter-jet:before{content:"\f0fb"}.fa-beer:before{content:"\f0fc"}.fa-h-square:before{content:"\f0fd"}.fa-plus-square:before{content:"\f0fe"}.fa-angle-double-left:before{content:"\f100"}.fa-angle-double-right:before{content:"\f101"}.fa-angle-double-up:before{content:"\f102"}.fa-angle-double-down:before{content:"\f103"}.fa-angle-left:before{content:"\f104"}.fa-angle-right:before{content:"\f105"}.fa-angle-up:before{content:"\f106"}.fa-angle-down:before{content:"\f107"}.fa-desktop:before{content:"\f108"}.fa-laptop:before{content:"\f109"}.fa-tablet:before{content:"\f10a"}.fa-mobile-phone:before,.fa-mobile:before{content:"\f10b"}.fa-circle-o:before{content:"\f10c"}.fa-quote-left:before{content:"\f10d"}.fa-quote-right:before{content:"\f10e"}.fa-spinner:before{content:"\f110"}.fa-circle:before{content:"\f111"}.fa-mail-reply:before,.fa-reply:before{content:"\f112"}.fa-github-alt:before{content:"\f113"}.fa-folder-o:before{content:"\f114"}.fa-folder-open-o:before{content:"\f115"}.fa-smile-o:before{content:"\f118"}.fa-frown-o:before{content:"\f119"}.fa-meh-o:before{content:"\f11a"}.fa-gamepad:before{content:"\f11b"}.fa-keyboard-o:before{content:"\f11c"}.fa-flag-o:before{content:"\f11d"}.fa-flag-checkered:before{content:"\f11e"}.fa-terminal:before{content:"\f120"}.fa-code:before{content:"\f121"}.fa-mail-reply-all:before,.fa-reply-all:before{content:"\f122"}.fa-star-half-empty:before,.fa-star-half-full:before,.fa-star-half-o:before{content:"\f123"}.fa-location-arrow:before{content:"\f124"}.fa-crop:before{content:"\f125"}.fa-code-fork:before{content:"\f126"}.fa-chain-broken:before,.fa-unlink:before{content:"\f127"}.fa-question:before{content:"\f128"}.fa-info:before{content:"\f129"}.fa-exclamation:before{content:"\f12a"}.fa-superscript:before{content:"\f12b"}.fa-subscript:before{content:"\f12c"}.fa-eraser:before{content:"\f12d"}.fa-puzzle-piece:before{content:"\f12e"}.fa-microphone:before{content:"\f130"}.fa-microphone-slash:before{content:"\f131"}.fa-shield:before{content:"\f132"}.fa-calendar-o:before{content:"\f133"}.fa-fire-extinguisher:before{content:"\f134"}.fa-rocket:before{content:"\f135"}.fa-maxcdn:before{content:"\f136"}.fa-chevron-circle-left:before{content:"\f137"}.fa-chevron-circle-right:before{content:"\f138"}.fa-chevron-circle-up:before{content:"\f139"}.fa-chevron-circle-down:before{content:"\f13a"}.fa-html5:before{content:"\f13b"}.fa-css3:before{content:"\f13c"}.fa-anchor:before{content:"\f13d"}.fa-unlock-alt:before{content:"\f13e"}.fa-bullseye:before{content:"\f140"}.fa-ellipsis-h:before{content:"\f141"}.fa-ellipsis-v:before{content:"\f142"}.fa-rss-square:before{content:"\f143"}.fa-play-circle:before{content:"\f144"}.fa-ticket:before{content:"\f145"}.fa-minus-square:before{content:"\f146"}.fa-minus-square-o:before{content:"\f147"}.fa-level-up:before{content:"\f148"}.fa-level-down:before{content:"\f149"}.fa-check-square:before{content:"\f14a"}.fa-pencil-square:before{content:"\f14b"}.fa-external-link-square:before{content:"\f14c"}.fa-share-square:before{content:"\f14d"}.fa-compass:before{content:"\f14e"}.fa-caret-square-o-down:before,.fa-toggle-down:before{content:"\f150"}.fa-caret-square-o-up:before,.fa-toggle-up:before{content:"\f151"}.fa-caret-square-o-right:before,.fa-toggle-right:before{content:"\f152"}.fa-eur:before,.fa-euro:before{content:"\f153"}.fa-gbp:before{content:"\f154"}.fa-dollar:before,.fa-usd:before{content:"\f155"}.fa-inr:before,.fa-rupee:before{content:"\f156"}.fa-cny:before,.fa-jpy:before,.fa-rmb:before,.fa-yen:before{content:"\f157"}.fa-rouble:before,.fa-rub:before,.fa-ruble:before{content:"\f158"}.fa-krw:before,.fa-won:before{content:"\f159"}.fa-bitcoin:before,.fa-btc:before{content:"\f15a"}.fa-file:before{content:"\f15b"}.fa-file-text:before{content:"\f15c"}.fa-sort-alpha-asc:before{content:"\f15d"}.fa-sort-alpha-desc:before{content:"\f15e"}.fa-sort-amount-asc:before{content:"\f160"}.fa-sort-amount-desc:before{content:"\f161"}.fa-sort-numeric-asc:before{content:"\f162"}.fa-sort-numeric-desc:before{content:"\f163"}.fa-thumbs-up:before{content:"\f164"}.fa-thumbs-down:before{content:"\f165"}.fa-youtube-square:before{content:"\f166"}.fa-youtube:before{content:"\f167"}.fa-xing:before{content:"\f168"}.fa-xing-square:before{content:"\f169"}.fa-youtube-play:before{content:"\f16a"}.fa-dropbox:before{content:"\f16b"}.fa-stack-overflow:before{content:"\f16c"}.fa-instagram:before{content:"\f16d"}.fa-flickr:before{content:"\f16e"}.fa-adn:before{content:"\f170"}.fa-bitbucket:before{content:"\f171"}.fa-bitbucket-square:before{content:"\f172"}.fa-tumblr:before{content:"\f173"}.fa-tumblr-square:before{content:"\f174"}.fa-long-arrow-down:before{content:"\f175"}.fa-long-arrow-up:before{content:"\f176"}.fa-long-arrow-left:before{content:"\f177"}.fa-long-arrow-right:before{content:"\f178"}.fa-apple:before{content:"\f179"}.fa-windows:before{content:"\f17a"}.fa-android:before{content:"\f17b"}.fa-linux:before{content:"\f17c"}.fa-dribbble:before{content:"\f17d"}.fa-skype:before{content:"\f17e"}.fa-foursquare:before{content:"\f180"}.fa-trello:before{content:"\f181"}.fa-female:before{content:"\f182"}.fa-male:before{content:"\f183"}.fa-gittip:before{content:"\f184"}.fa-sun-o:before{content:"\f185"}.fa-moon-o:before{content:"\f186"}.fa-archive:before{content:"\f187"}.fa-bug:before{content:"\f188"}.fa-vk:before{content:"\f189"}.fa-weibo:before{content:"\f18a"}.fa-renren:before{content:"\f18b"}.fa-pagelines:before{content:"\f18c"}.fa-stack-exchange:before{content:"\f18d"}.fa-arrow-circle-o-right:before{content:"\f18e"}.fa-arrow-circle-o-left:before{content:"\f190"}.fa-caret-square-o-left:before,.fa-toggle-left:before{content:"\f191"}.fa-dot-circle-o:before{content:"\f192"}.fa-wheelchair:before{content:"\f193"}.fa-vimeo-square:before{content:"\f194"}.fa-try:before,.fa-turkish-lira:before{content:"\f195"}.fa-plus-square-o:before{content:"\f196"}.fa-space-shuttle:before{content:"\f197"}.fa-slack:before{content:"\f198"}.fa-envelope-square:before{content:"\f199"}.fa-wordpress:before{content:"\f19a"}.fa-openid:before{content:"\f19b"}.fa-bank:before,.fa-institution:before,.fa-university:before{content:"\f19c"}.fa-graduation-cap:before,.fa-mortar-board:before{content:"\f19d"}.fa-yahoo:before{content:"\f19e"}.fa-google:before{content:"\f1a0"}.fa-reddit:before{content:"\f1a1"}.fa-reddit-square:before{content:"\f1a2"}.fa-stumbleupon-circle:before{content:"\f1a3"}.fa-stumbleupon:before{content:"\f1a4"}.fa-delicious:before{content:"\f1a5"}.fa-digg:before{content:"\f1a6"}.fa-pied-piper:before{content:"\f1a7"}.fa-pied-piper-alt:before{content:"\f1a8"}.fa-drupal:before{content:"\f1a9"}.fa-joomla:before{content:"\f1aa"}.fa-language:before{content:"\f1ab"}.fa-fax:before{content:"\f1ac"}.fa-building:before{content:"\f1ad"}.fa-child:before{content:"\f1ae"}.fa-paw:before{content:"\f1b0"}.fa-spoon:before{content:"\f1b1"}.fa-cube:before{content:"\f1b2"}.fa-cubes:before{content:"\f1b3"}.fa-behance:before{content:"\f1b4"}.fa-behance-square:before{content:"\f1b5"}.fa-steam:before{content:"\f1b6"}.fa-steam-square:before{content:"\f1b7"}.fa-recycle:before{content:"\f1b8"}.fa-automobile:before,.fa-car:before{content:"\f1b9"}.fa-cab:before,.fa-taxi:before{content:"\f1ba"}.fa-tree:before{content:"\f1bb"}.fa-spotify:before{content:"\f1bc"}.fa-deviantart:before{content:"\f1bd"}.fa-soundcloud:before{content:"\f1be"}.fa-database:before{content:"\f1c0"}.fa-file-pdf-o:before{content:"\f1c1"}.fa-file-word-o:before{content:"\f1c2"}.fa-file-excel-o:before{content:"\f1c3"}.fa-file-powerpoint-o:before{content:"\f1c4"}.fa-file-image-o:before,.fa-file-photo-o:before,.fa-file-picture-o:before{content:"\f1c5"}.fa-file-archive-o:before,.fa-file-zip-o:before{content:"\f1c6"}.fa-file-audio-o:before,.fa-file-sound-o:before{content:"\f1c7"}.fa-file-movie-o:before,.fa-file-video-o:before{content:"\f1c8"}.fa-file-code-o:before{content:"\f1c9"}.fa-vine:before{content:"\f1ca"}.fa-codepen:before{content:"\f1cb"}.fa-jsfiddle:before{content:"\f1cc"}.fa-life-bouy:before,.fa-life-buoy:before,.fa-life-ring:before,.fa-life-saver:before,.fa-support:before{content:"\f1cd"}.fa-circle-o-notch:before{content:"\f1ce"}.fa-ra:before,.fa-rebel:before{content:"\f1d0"}.fa-empire:before,.fa-ge:before{content:"\f1d1"}.fa-git-square:before{content:"\f1d2"}.fa-git:before{content:"\f1d3"}.fa-hacker-news:before{content:"\f1d4"}.fa-tencent-weibo:before{content:"\f1d5"}.fa-qq:before{content:"\f1d6"}.fa-wechat:before,.fa-weixin:before{content:"\f1d7"}.fa-paper-plane:before,.fa-send:before{content:"\f1d8"}.fa-paper-plane-o:before,.fa-send-o:before{content:"\f1d9"}.fa-history:before{content:"\f1da"}.fa-circle-thin:before{content:"\f1db"}.fa-header:before{content:"\f1dc"}.fa-paragraph:before{content:"\f1dd"}.fa-sliders:before{content:"\f1de"}.fa-share-alt:before{content:"\f1e0"}.fa-share-alt-square:before{content:"\f1e1"}.fa-bomb:before{content:"\f1e2"}.fa-futbol-o:before,.fa-soccer-ball-o:before{content:"\f1e3"}.fa-tty:before{content:"\f1e4"}.fa-binoculars:before{content:"\f1e5"}.fa-plug:before{content:"\f1e6"}.fa-slideshare:before{content:"\f1e7"}.fa-twitch:before{content:"\f1e8"}.fa-yelp:before{content:"\f1e9"}.fa-newspaper-o:before{content:"\f1ea"}.fa-wifi:before{content:"\f1eb"}.fa-calculator:before{content:"\f1ec"}.fa-paypal:before{content:"\f1ed"}.fa-google-wallet:before{content:"\f1ee"}.fa-cc-visa:before{content:"\f1f0"}.fa-cc-mastercard:before{content:"\f1f1"}.fa-cc-discover:before{content:"\f1f2"}.fa-cc-amex:before{content:"\f1f3"}.fa-cc-paypal:before{content:"\f1f4"}.fa-cc-stripe:before{content:"\f1f5"}.fa-bell-slash:before{content:"\f1f6"}.fa-bell-slash-o:before{content:"\f1f7"}.fa-trash:before{content:"\f1f8"}.fa-copyright:before{content:"\f1f9"}.fa-at:before{content:"\f1fa"}.fa-eyedropper:before{content:"\f1fb"}.fa-paint-brush:before{content:"\f1fc"}.fa-birthday-cake:before{content:"\f1fd"}.fa-area-chart:before{content:"\f1fe"}.fa-pie-chart:before{content:"\f200"}.fa-line-chart:before{content:"\f201"}.fa-lastfm:before{content:"\f202"}.fa-lastfm-square:before{content:"\f203"}.fa-toggle-off:before{content:"\f204"}.fa-toggle-on:before{content:"\f205"}.fa-bicycle:before{content:"\f206"}.fa-bus:before{content:"\f207"}.fa-ioxhost:before{content:"\f208"}.fa-angellist:before{content:"\f209"}.fa-cc:before{content:"\f20a"}.fa-ils:before,.fa-shekel:before,.fa-sheqel:before{content:"\f20b"}.fa-meanpath:before{content:"\f20c"}/*!
*
* IPython base
*
*/.modal.fade .modal-dialog{-webkit-transform:translate(0,0);-ms-transform:translate(0,0);-o-transform:translate(0,0);transform:translate(0,0)}code{color:#000}pre{font-size:inherit;line-height:inherit}label{font-weight:400}.border-box-sizing{box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box}.corner-all{border-radius:2px}.no-padding{padding:0}.hbox{display:-webkit-box;-webkit-box-orient:horizontal;display:-moz-box;-moz-box-orient:horizontal;display:box;box-orient:horizontal;box-align:stretch;display:flex;flex-direction:row;align-items:stretch}.hbox>*{-webkit-box-flex:0;-moz-box-flex:0;box-flex:0;flex:none}.vbox{display:-webkit-box;-webkit-box-orient:vertical;display:-moz-box;-moz-box-orient:vertical;display:box;box-orient:vertical;box-align:stretch;display:flex;flex-direction:column;align-items:stretch}.vbox>*{-webkit-box-flex:0;-moz-box-flex:0;box-flex:0;flex:none}.hbox.reverse,.reverse,.vbox.reverse{-webkit-box-direction:reverse;-moz-box-direction:reverse;box-direction:reverse;flex-direction:row-reverse}.box-flex0,.hbox.box-flex0,.vbox.box-flex0{-webkit-box-flex:0;-moz-box-flex:0;box-flex:0;flex:none;width:auto}.box-flex1,.hbox.box-flex1,.vbox.box-flex1{-webkit-box-flex:1;-moz-box-flex:1;box-flex:1;flex:1}.box-flex,.hbox.box-flex,.vbox.box-flex{-webkit-box-flex:1;-moz-box-flex:1;box-flex:1;flex:1}.box-flex2,.hbox.box-flex2,.vbox.box-flex2{-webkit-box-flex:2;-moz-box-flex:2;box-flex:2;flex:2}.box-group1{-webkit-box-flex-group:1;-moz-box-flex-group:1;box-flex-group:1}.box-group2{-webkit-box-flex-group:2;-moz-box-flex-group:2;box-flex-group:2}.hbox.start,.start,.vbox.start{-webkit-box-pack:start;-moz-box-pack:start;box-pack:start;justify-content:flex-start}.end,.hbox.end,.vbox.end{-webkit-box-pack:end;-moz-box-pack:end;box-pack:end;justify-content:flex-end}.center,.hbox.center,.vbox.center{-webkit-box-pack:center;-moz-box-pack:center;box-pack:center;justify-content:center}.baseline,.hbox.baseline,.vbox.baseline{-webkit-box-pack:baseline;-moz-box-pack:baseline;box-pack:baseline;justify-content:baseline}.hbox.stretch,.stretch,.vbox.stretch{-webkit-box-pack:stretch;-moz-box-pack:stretch;box-pack:stretch;justify-content:stretch}.align-start,.hbox.align-start,.vbox.align-start{-webkit-box-align:start;-moz-box-align:start;box-align:start;align-items:flex-start}.align-end,.hbox.align-end,.vbox.align-end{-webkit-box-align:end;-moz-box-align:end;box-align:end;align-items:flex-end}.align-center,.hbox.align-center,.vbox.align-center{-webkit-box-align:center;-moz-box-align:center;box-align:center;align-items:center}.align-baseline,.hbox.align-baseline,.vbox.align-baseline{-webkit-box-align:baseline;-moz-box-align:baseline;box-align:baseline;align-items:baseline}.align-stretch,.hbox.align-stretch,.vbox.align-stretch{-webkit-box-align:stretch;-moz-box-align:stretch;box-align:stretch;align-items:stretch}div.error{margin:2em;text-align:center}div.error>h1{font-size:500%;line-height:normal}div.error>p{font-size:200%;line-height:normal}div.traceback-wrapper{text-align:left;max-width:800px;margin:auto}body{position:absolute;left:0;right:0;top:0;bottom:0;overflow:visible}#header{display:none;background-color:#fff;position:relative;z-index:100}#header #header-container{padding-bottom:5px;padding-top:5px;box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box}#header .header-bar{width:100%;height:1px;background:#e7e7e7;margin-bottom:-1px}#header-spacer{width:100%;visibility:hidden}@media print{#header{display:none!important}#header-spacer{display:none}}#ipython_notebook{padding-left:0;padding-top:1px;padding-bottom:1px}@media (max-width:991px){#ipython_notebook{margin-left:10px}}#noscript{width:auto;padding-top:16px;padding-bottom:16px;text-align:center;font-size:22px;color:red;font-weight:700}#ipython_notebook img{height:28px}#site{width:100%;display:none;box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box;overflow:auto}@media print{#site{height:auto!important}}.ui-button .ui-button-text{padding:.2em .8em;font-size:77%}input.ui-button{padding:.3em .9em}span#login_widget{float:right}#logout,span#login_widget>.button{color:#333;background-color:#fff;border-color:#ccc}#logout.active,#logout.focus,#logout:active,#logout:focus,#logout:hover,.open>.dropdown-toggle#logout,.open>.dropdown-togglespan#login_widget>.button,span#login_widget>.button.active,span#login_widget>.button.focus,span#login_widget>.button:active,span#login_widget>.button:focus,span#login_widget>.button:hover{color:#333;background-color:#e6e6e6;border-color:#adadad}#logout.active,#logout:active,.open>.dropdown-toggle#logout,.open>.dropdown-togglespan#login_widget>.button,span#login_widget>.button.active,span#login_widget>.button:active{background-image:none}#logout.disabled,#logout.disabled.active,#logout.disabled.focus,#logout.disabled:active,#logout.disabled:focus,#logout.disabled:hover,#logout[disabled],#logout[disabled].active,#logout[disabled].focus,#logout[disabled]:active,#logout[disabled]:focus,#logout[disabled]:hover,fieldset[disabled] #logout,fieldset[disabled] #logout.active,fieldset[disabled] #logout.focus,fieldset[disabled] #logout:active,fieldset[disabled] #logout:focus,fieldset[disabled] #logout:hover,fieldset[disabled] span#login_widget>.button,fieldset[disabled] span#login_widget>.button.active,fieldset[disabled] span#login_widget>.button.focus,fieldset[disabled] span#login_widget>.button:active,fieldset[disabled] span#login_widget>.button:focus,fieldset[disabled] span#login_widget>.button:hover,span#login_widget>.button.disabled,span#login_widget>.button.disabled.active,span#login_widget>.button.disabled.focus,span#login_widget>.button.disabled:active,span#login_widget>.button.disabled:focus,span#login_widget>.button.disabled:hover,span#login_widget>.button[disabled],span#login_widget>.button[disabled].active,span#login_widget>.button[disabled].focus,span#login_widget>.button[disabled]:active,span#login_widget>.button[disabled]:focus,span#login_widget>.button[disabled]:hover{background-color:#fff;border-color:#ccc}#logout .badge,span#login_widget>.button .badge{color:#fff;background-color:#333}.nav-header{text-transform:none}#header>span{margin-top:10px}.modal_stretch .modal-dialog{display:-webkit-box;-webkit-box-orient:vertical;display:-moz-box;-moz-box-orient:vertical;display:box;box-orient:vertical;box-align:stretch;display:flex;flex-direction:column;align-items:stretch;min-height:80vh}.modal_stretch .modal-dialog .modal-body{max-height:calc(100vh - 200px);overflow:auto;flex:1}@media (min-width:768px){.modal .modal-dialog{width:700px}select.form-control{margin-left:12px;margin-right:12px}}/*!
*
* IPython auth
*
*/.center-nav{display:inline-block;margin-bottom:-4px}/*!
*
* IPython tree view
*
*/.alternate_upload{background-color:none;display:inline}.alternate_upload.form{padding:0;margin:0}.alternate_upload input.fileinput{text-align:center;vertical-align:middle;display:inline;opacity:0;z-index:2;width:12ex;margin-right:-12ex}.alternate_upload .btn-upload{height:22px}ul#tabs{margin-bottom:4px}ul#tabs a{padding-top:6px;padding-bottom:4px}ul.breadcrumb a:focus,ul.breadcrumb a:hover{text-decoration:none}ul.breadcrumb i.icon-home{font-size:16px;margin-right:4px}ul.breadcrumb span{color:#5e5e5e}.list_toolbar{padding:4px 0;vertical-align:middle}.list_toolbar .tree-buttons{padding-top:1px}.dynamic-buttons{padding-top:3px;display:inline-block}.list_toolbar [class*=span]{min-height:24px}.list_header{font-weight:700;background-color:#eee}.list_placeholder{font-weight:700;padding:4px 7px}.list_container{margin-top:4px;margin-bottom:20px;border:1px solid #ddd;border-radius:2px}.list_container>div{border-bottom:1px solid #ddd}.list_container>div:hover .list-item{background-color:red}.list_container>div:last-child{border:none}.list_item:hover .list_item{background-color:#ddd}.list_item a{text-decoration:none}.list_item:hover{background-color:#fafafa}.action_col{text-align:right}.list_header>div,.list_item>div{line-height:22px;padding:4px 7px}.list_header>div input,.list_item>div input{margin-right:7px;margin-left:14px;vertical-align:baseline;line-height:22px;position:relative;top:-1px}.list_header>div .item_link,.list_item>div .item_link{margin-left:-1px;vertical-align:baseline;line-height:22px}.new-file input[type=checkbox]{visibility:hidden}.item_name{line-height:22px;height:24px}.item_icon{font-size:14px;color:#5e5e5e;margin-right:7px;margin-left:7px;line-height:22px;vertical-align:baseline}.item_buttons{line-height:1em;margin-left:-5px}.item_buttons .btn-group,.item_buttons .input-group{float:left}.item_buttons>.btn,.item_buttons>.btn-group,.item_buttons>.input-group{margin-left:5px}.item_buttons .btn{min-width:13ex}.item_buttons .running-indicator{padding-top:4px;color:#5cb85c}.toolbar_info{height:24px;line-height:24px}input.engine_num_input,input.nbname_input{padding-top:3px;padding-bottom:3px;height:22px;line-height:14px;margin:0}input.engine_num_input{width:60px}.highlight_text{color:#00f}#project_name{display:inline-block;padding-left:7px;margin-left:-2px}#project_name>.breadcrumb{padding:0;margin-bottom:0;background-color:transparent;font-weight:700}#tree-selector{padding-right:0}#button-select-all{min-width:50px}#select-all{margin-left:7px;margin-right:2px}.menu_icon{margin-right:2px}.tab-content .row{margin-left:0;margin-right:0}.folder_icon:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:"\f114"}.folder_icon:before.pull-left{margin-right:.3em}.folder_icon:before.pull-right{margin-left:.3em}.notebook_icon:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:"\f02d";position:relative;top:-1px}.notebook_icon:before.pull-left{margin-right:.3em}.notebook_icon:before.pull-right{margin-left:.3em}.running_notebook_icon:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:"\f02d";position:relative;top:-1px;color:#5cb85c}.running_notebook_icon:before.pull-left{margin-right:.3em}.running_notebook_icon:before.pull-right{margin-left:.3em}.file_icon:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:"\f016";position:relative;top:-2px}.file_icon:before.pull-left{margin-right:.3em}.file_icon:before.pull-right{margin-left:.3em}#notebook_toolbar .pull-right{padding-top:0;margin-right:-1px}ul#new-menu{left:auto;right:0}.kernel-menu-icon{padding-right:12px;width:24px;content:"\f096"}.kernel-menu-icon:before{content:"\f096"}.kernel-menu-icon-current:before{content:"\f00c"}#tab_content{padding-top:20px}#running .panel-group .panel{margin-top:3px;margin-bottom:1em}#running .panel-group .panel .panel-heading{background-color:#eee;line-height:22px;padding:4px 7px}#running .panel-group .panel .panel-heading a:focus,#running .panel-group .panel .panel-heading a:hover{text-decoration:none}#running .panel-group .panel .panel-body{padding:0}#running .panel-group .panel .panel-body .list_container{margin-top:0;margin-bottom:0;border:0;border-radius:0}#running .panel-group .panel .panel-body .list_container .list_item{border-bottom:1px solid #ddd}#running .panel-group .panel .panel-body .list_container .list_item:last-child{border-bottom:0}.delete-button,.duplicate-button,.rename-button,.shutdown-button{display:none}.dynamic-instructions{display:inline-block;padding-top:4px}/*!
*
* IPython text editor webapp
*
*/.selected-keymap i.fa{padding:0 5px}.selected-keymap i.fa:before{content:"\f00c"}#mode-menu{overflow:auto;max-height:20em}.edit_app #header{-webkit-box-shadow:0 0 12px 1px rgba(87,87,87,.2);box-shadow:0 0 12px 1px rgba(87,87,87,.2)}.edit_app #menubar .navbar{margin-bottom:-1px}.dirty-indicator{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;width:20px}.dirty-indicator.pull-left{margin-right:.3em}.dirty-indicator.pull-right{margin-left:.3em}.dirty-indicator-dirty{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;width:20px}.dirty-indicator-dirty.pull-left{margin-right:.3em}.dirty-indicator-dirty.pull-right{margin-left:.3em}.dirty-indicator-clean{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;width:20px}.dirty-indicator-clean.pull-left{margin-right:.3em}.dirty-indicator-clean.pull-right{margin-left:.3em}.dirty-indicator-clean:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:"\f00c"}.dirty-indicator-clean:before.pull-left{margin-right:.3em}.dirty-indicator-clean:before.pull-right{margin-left:.3em}#filename{font-size:16pt;display:table;padding:0 5px}#current-mode{padding-left:5px;padding-right:5px}#texteditor-backdrop{padding-top:20px;padding-bottom:20px}@media not print{#texteditor-backdrop{background-color:#eee}}@media print{#texteditor-backdrop #texteditor-container .CodeMirror-gutter,#texteditor-backdrop #texteditor-container .CodeMirror-gutters{background-color:#fff}}@media not print{#texteditor-backdrop #texteditor-container .CodeMirror-gutter,#texteditor-backdrop #texteditor-container .CodeMirror-gutters{background-color:#fff}#texteditor-backdrop #texteditor-container{padding:0;background-color:#fff;-webkit-box-shadow:0 0 12px 1px rgba(87,87,87,.2);box-shadow:0 0 12px 1px rgba(87,87,87,.2)}}/*!
*
* IPython notebook
*
*/.ansibold{font-weight:700}.ansiblack{color:#000}.ansired{color:#8b0000}.ansigreen{color:#006400}.ansiyellow{color:#c4a000}.ansiblue{color:#00008b}.ansipurple{color:#9400d3}.ansicyan{color:#4682b4}.ansigray{color:gray}.ansibgblack{background-color:#000}.ansibgred{background-color:red}.ansibggreen{background-color:green}.ansibgyellow{background-color:#ff0}.ansibgblue{background-color:#00f}.ansibgpurple{background-color:#ff00ff}.ansibgcyan{background-color:#0ff}.ansibggray{background-color:gray}div.cell{border:1px solid transparent;display:-webkit-box;-webkit-box-orient:vertical;display:-moz-box;-moz-box-orient:vertical;display:box;box-orient:vertical;box-align:stretch;display:flex;flex-direction:column;align-items:stretch;border-radius:2px;box-sizing:border-box;-moz-box-sizing:border-box;border-width:thin;border-style:solid;width:100%;padding:5px;margin:0;outline:0}div.cell.selected{border-color:#ababab}@media print{div.cell.selected{border-color:transparent}}.edit_mode div.cell.selected{border-color:green}.prompt{min-width:14ex;padding:.4em;margin:0;font-family:monospace;text-align:right;line-height:1.21429em}div.inner_cell{display:-webkit-box;-webkit-box-orient:vertical;display:-moz-box;-moz-box-orient:vertical;display:box;box-orient:vertical;box-align:stretch;display:flex;flex-direction:column;align-items:stretch;-webkit-box-flex:1;-moz-box-flex:1;box-flex:1;flex:1}@-moz-document url-prefix(){div.inner_cell{overflow-x:hidden}}div.input_area{border:1px solid #cfcfcf;border-radius:2px;background:#f7f7f7;line-height:1.21429em}div.prompt:empty{padding-top:0;padding-bottom:0}div.unrecognized_cell{padding:5px 5px 5px 0;display:-webkit-box;-webkit-box-orient:horizontal;display:-moz-box;-moz-box-orient:horizontal;display:box;box-orient:horizontal;box-align:stretch;display:flex;flex-direction:row;align-items:stretch}div.unrecognized_cell .inner_cell{border-radius:2px;padding:5px;font-weight:700;color:red;border:1px solid #cfcfcf;background:#eaeaea}div.unrecognized_cell .inner_cell a,div.unrecognized_cell .inner_cell a:hover{color:inherit;text-decoration:none}@media (max-width:540px){.prompt{text-align:left}div.unrecognized_cell>div.prompt{display:none}}div.code_cell{}div.input{page-break-inside:avoid;display:-webkit-box;-webkit-box-orient:horizontal;display:-moz-box;-moz-box-orient:horizontal;display:box;box-orient:horizontal;box-align:stretch;display:flex;flex-direction:row;align-items:stretch}@media (max-width:540px){div.input{-webkit-box-orient:vertical;-moz-box-orient:vertical;box-orient:vertical;box-align:stretch;display:flex;flex-direction:column;align-items:stretch}}div.input_prompt{color:navy;border-top:1px solid transparent}div.input_area>div.highlight{margin:.4em;border:none;padding:0;background-color:transparent}div.input_area>div.highlight>pre{margin:0;border:none;padding:0;background-color:transparent}.CodeMirror{line-height:1.21429em;font-size:14px;height:auto;background:0 0}.CodeMirror-scroll{overflow-y:hidden;overflow-x:auto}.CodeMirror-lines{padding:.4em}.CodeMirror-linenumber{padding:0 8px 0 4px}.CodeMirror-gutters{border-bottom-left-radius:2px;border-top-left-radius:2px}.CodeMirror pre{padding:0;border:0;border-radius:0}.highlight-base,.highlight-variable{color:#000}.highlight-variable-2{color:#1a1a1a}.highlight-variable-3{color:#333}.highlight-string{color:#BA2121}.highlight-comment{color:#408080;font-style:italic}.highlight-number{color:#080}.highlight-atom{color:#88F}.highlight-keyword{color:green;font-weight:700}.highlight-builtin{color:green}.highlight-error{color:red}.highlight-operator{color:#A2F;font-weight:700}.highlight-meta{color:#A2F}.highlight-def{color:#00f}.highlight-string-2{color:#f50}.highlight-qualifier{color:#555}.highlight-bracket{color:#997}.highlight-tag{color:#170}.highlight-attribute{color:#00c}.highlight-header{color:#00f}.highlight-quote{color:#090}.highlight-link{color:#00c}.cm-s-ipython span.cm-keyword{color:green;font-weight:700}.cm-s-ipython span.cm-atom{color:#88F}.cm-s-ipython span.cm-number{color:#080}.cm-s-ipython span.cm-def{color:#00f}.cm-s-ipython span.cm-variable{color:#000}.cm-s-ipython span.cm-operator{color:#A2F;font-weight:700}.cm-s-ipython span.cm-variable-2{color:#1a1a1a}.cm-s-ipython span.cm-variable-3{color:#333}.cm-s-ipython span.cm-comment{color:#408080;font-style:italic}.cm-s-ipython span.cm-string{color:#BA2121}.cm-s-ipython span.cm-string-2{color:#f50}.cm-s-ipython span.cm-meta{color:#A2F}.cm-s-ipython span.cm-qualifier{color:#555}.cm-s-ipython span.cm-builtin{color:green}.cm-s-ipython span.cm-bracket{color:#997}.cm-s-ipython span.cm-tag{color:#170}.cm-s-ipython span.cm-attribute{color:#00c}.cm-s-ipython span.cm-header{color:#00f}.cm-s-ipython span.cm-quote{color:#090}.cm-s-ipython span.cm-link{color:#00c}.cm-s-ipython span.cm-error{color:red}.cm-s-ipython span.cm-tab{background:url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=')right no-repeat}div.output_wrapper{display:-webkit-box;-webkit-box-align:stretch;display:-moz-box;-moz-box-align:stretch;display:box;box-orient:vertical;box-align:stretch;display:flex;flex-direction:column;align-items:stretch;z-index:1}div.output_scroll{height:24em;width:100%;overflow:auto;border-radius:2px;-webkit-box-shadow:inset 0 2px 8px rgba(0,0,0,.8);box-shadow:inset 0 2px 8px rgba(0,0,0,.8);display:block}div.output_collapsed{margin:0;padding:0;display:-webkit-box;-webkit-box-orient:vertical;display:-moz-box;-moz-box-orient:vertical;display:box;box-orient:vertical;box-align:stretch;display:flex;flex-direction:column;align-items:stretch}div.out_prompt_overlay{height:100%;padding:0 .4em;position:absolute;border-radius:2px}div.out_prompt_overlay:hover{-webkit-box-shadow:inset 0 0 1px #000;box-shadow:inset 0 0 1px #000;background:rgba(240,240,240,.5)}div.output_prompt{color:#8b0000}div.output_area{padding:0;page-break-inside:avoid;display:-webkit-box;-webkit-box-orient:horizontal;display:-moz-box;-moz-box-orient:horizontal;display:box;box-orient:horizontal;box-align:stretch;display:flex;flex-direction:row;align-items:stretch}div.output_area .MathJax_Display{text-align:left!important}div.output_area .rendered_html img,div.output_area .rendered_html table{margin-left:0;margin-right:0}div.output_area img,div.output_area svg{max-width:100%;height:auto}div.output_area img.unconfined,div.output_area svg.unconfined{max-width:none}.output{display:-webkit-box;-webkit-box-orient:vertical;display:-moz-box;-moz-box-orient:vertical;display:box;box-orient:vertical;box-align:stretch;display:flex;flex-direction:column;align-items:stretch}@media (max-width:540px){div.output_area{-webkit-box-orient:vertical;-moz-box-orient:vertical;box-orient:vertical;box-align:stretch;display:flex;flex-direction:column;align-items:stretch}}div.output_area pre{margin:0;padding:0;border:0;vertical-align:baseline;color:#000;background-color:transparent;border-radius:0}div.output_subarea{overflow-x:auto;padding:.4em;-webkit-box-flex:1;-moz-box-flex:1;box-flex:1;flex:1;max-width:calc(100% - 14ex)}div.output_text{text-align:left;color:#000;line-height:1.21429em}div.output_stderr{background:#fdd}div.output_latex{text-align:left}div.output_javascript:empty{padding:0}.js-error{color:#8b0000}div.raw_input_container{font-family:monospace;padding-top:5px}span.raw_input_prompt{}input.raw_input{font-family:inherit;font-size:inherit;color:inherit;width:auto;vertical-align:baseline;padding:0 .25em;margin:0 .25em}input.raw_input:focus{box-shadow:none}p.p-space{margin-bottom:10px}div.output_unrecognized{padding:5px;font-weight:700;color:red}div.output_unrecognized a,div.output_unrecognized a:hover{color:inherit;text-decoration:none}.rendered_html{color:#000}.rendered_html em{font-style:italic}.rendered_html strong{font-weight:700}.rendered_html :link,.rendered_html :visited,.rendered_html u{text-decoration:underline}.rendered_html h1{font-size:185.7%;margin:1.08em 0 0;font-weight:700;line-height:1}.rendered_html h2{font-size:157.1%;margin:1.27em 0 0;font-weight:700;line-height:1}.rendered_html h3{font-size:128.6%;margin:1.55em 0 0;font-weight:700;line-height:1}.rendered_html h4{font-size:100%;margin:2em 0 0;font-weight:700;line-height:1}.rendered_html h5,.rendered_html h6{font-size:100%;margin:2em 0 0;font-weight:700;line-height:1;font-style:italic}.rendered_html h1:first-child{margin-top:.538em}.rendered_html h2:first-child{margin-top:.636em}.rendered_html h3:first-child{margin-top:.777em}.rendered_html h4:first-child,.rendered_html h5:first-child,.rendered_html h6:first-child{margin-top:1em}.rendered_html ul{list-style:disc;margin:0 2em;padding-left:0}.rendered_html ul ul{list-style:square;margin:0 2em}.rendered_html ul ul ul{list-style:circle;margin:0 2em}.rendered_html ol{list-style:decimal;margin:0 2em;padding-left:0}.rendered_html ol ol{list-style:upper-alpha;margin:0 2em}.rendered_html ol ol ol{list-style:lower-alpha;margin:0 2em}.rendered_html ol ol ol ol{list-style:lower-roman;margin:0 2em}.rendered_html ol ol ol ol ol{list-style:decimal;margin:0 2em}.rendered_html *+ol,.rendered_html *+ul{margin-top:1em}.rendered_html hr{color:#000;background-color:#000}.rendered_html pre{margin:1em 2em}.rendered_html code,.rendered_html pre{border:0;background-color:#fff;color:#000;font-size:100%;padding:0}.rendered_html blockquote{margin:1em 2em}.rendered_html table{margin-left:auto;margin-right:auto;border:1px solid #000;border-collapse:collapse}.rendered_html td,.rendered_html th,.rendered_html tr{border:1px solid #000;border-collapse:collapse;margin:1em 2em}.rendered_html td,.rendered_html th{text-align:left;vertical-align:middle;padding:4px}.rendered_html th{font-weight:700}.rendered_html *+table{margin-top:1em}.rendered_html p{text-align:left}.rendered_html *+p{margin-top:1em}.rendered_html img{display:block;margin-left:auto;margin-right:auto}.rendered_html *+img{margin-top:1em}.rendered_html img,.rendered_html svg{max-width:100%;height:auto}.rendered_html img.unconfined,.rendered_html svg.unconfined{max-width:none}div.text_cell{display:-webkit-box;-webkit-box-orient:horizontal;display:-moz-box;-moz-box-orient:horizontal;display:box;box-orient:horizontal;box-align:stretch;display:flex;flex-direction:row;align-items:stretch}@media (max-width:540px){div.text_cell>div.prompt{display:none}}div.text_cell_render{outline:0;resize:none;width:inherit;border-style:none;padding:.5em .5em .5em .4em;color:#000;box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box}a.anchor-link:link{text-decoration:none;padding:0 20px;visibility:hidden}h1:hover .anchor-link,h2:hover .anchor-link,h3:hover .anchor-link,h4:hover .anchor-link,h5:hover .anchor-link,h6:hover .anchor-link{visibility:visible}.text_cell.rendered .input_area{display:none}.text_cell.rendered .rendered_html{overflow-x:auto}.text_cell.unrendered .text_cell_render{display:none}.cm-header-1,.cm-header-2,.cm-header-3,.cm-header-4,.cm-header-5,.cm-header-6{font-weight:700;font-family:"Helvetica Neue",Helvetica,Arial,sans-serif}.cm-header-1{font-size:185.7%}.cm-header-2{font-size:157.1%}.cm-header-3{font-size:128.6%}.cm-header-4{font-size:110%}.cm-header-5,.cm-header-6{font-size:100%;font-style:italic}/*!
*
* IPython notebook webapp
*
*/@media (max-width:767px){.notebook_app{padding-left:0;padding-right:0}}#ipython-main-app{box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box;height:100%}div#notebook_panel{margin:0;padding:0;box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box;height:100%}#notebook{font-size:14px;line-height:20px;overflow-y:hidden;overflow-x:auto;width:100%;padding-top:20px;margin:0;outline:0;box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box;min-height:100%}@media not print{#notebook-container{padding:15px;background-color:#fff;min-height:0;-webkit-box-shadow:0 0 12px 1px rgba(87,87,87,.2);box-shadow:0 0 12px 1px rgba(87,87,87,.2)}}div.ui-widget-content{border:1px solid #ababab;outline:0}pre.dialog{background-color:#f7f7f7;border:1px solid #ddd;border-radius:2px;padding:.4em .4em .4em 2em}p.dialog{padding:.2em}code,kbd,pre,samp{white-space:pre-wrap}#fonttest{font-family:monospace}p{margin-bottom:0}.end_space{min-height:100px;transition:height .2s ease}.notebook_app #header{-webkit-box-shadow:0 0 12px 1px rgba(87,87,87,.2);box-shadow:0 0 12px 1px rgba(87,87,87,.2)}@media not print{.notebook_app{background-color:#eee}}.celltoolbar{border:thin solid #CFCFCF;border-bottom:none;background:#EEE;border-radius:2px 2px 0 0;width:100%;height:29px;padding-right:4px;-webkit-box-orient:horizontal;-moz-box-orient:horizontal;box-orient:horizontal;box-align:stretch;display:flex;flex-direction:row;align-items:stretch;-webkit-box-pack:end;-moz-box-pack:end;box-pack:end;justify-content:flex-end;font-size:87%;padding-top:3px}@media print{.edit_mode div.cell.selected{border-color:transparent}div.code_cell{page-break-inside:avoid}#notebook-container{width:100%}.celltoolbar{display:none}}.ctb_hideshow{display:none;vertical-align:bottom}.ctb_global_show .ctb_show.ctb_hideshow{display:block}.ctb_global_show .ctb_show+.input_area,.ctb_global_show .ctb_show+div.text_cell_input,.ctb_global_show .ctb_show~div.text_cell_render{border-top-right-radius:0;border-top-left-radius:0}.ctb_global_show .ctb_show~div.text_cell_render{border:1px solid #cfcfcf}.celltoolbar select{color:#555;background-color:#fff;background-image:none;border:1px solid #ccc;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.075);box-shadow:inset 0 1px 1px rgba(0,0,0,.075);-webkit-transition:border-color ease-in-out .15s,box-shadow ease-in-out .15s;-o-transition:border-color ease-in-out .15s,box-shadow ease-in-out .15s;transition:border-color ease-in-out .15s,box-shadow ease-in-out .15s;line-height:1.5;border-radius:1px;width:inherit;font-size:inherit;height:22px;padding:0;display:inline-block}.celltoolbar select:focus{border-color:#66afe9;outline:0;-webkit-box-shadow:inset 0 1px 1px rgba(0,0,0,.075),0 0 8px rgba(102,175,233,.6);box-shadow:inset 0 1px 1px rgba(0,0,0,.075),0 0 8px rgba(102,175,233,.6)}.celltoolbar select::-moz-placeholder{color:#999;opacity:1}.celltoolbar select:-ms-input-placeholder{color:#999}.celltoolbar select::-webkit-input-placeholder{color:#999}.celltoolbar select[disabled],.celltoolbar select[readonly],fieldset[disabled] .celltoolbar select{background-color:#eee;opacity:1}.celltoolbar select[disabled],fieldset[disabled] .celltoolbar select{cursor:not-allowed}textarea.celltoolbar select{height:auto}select.celltoolbar select{height:30px;line-height:30px}select[multiple].celltoolbar select,textarea.celltoolbar select{height:auto}.celltoolbar label{margin-left:5px;margin-right:5px}.completions{position:absolute;z-index:10;overflow:hidden;border:1px solid #ababab;border-radius:2px;-webkit-box-shadow:0 6px 10px -1px #adadad;box-shadow:0 6px 10px -1px #adadad;line-height:1}.completions select{background:#fff;outline:0;border:none;padding:0;margin:0;overflow:auto;font-family:monospace;font-size:110%;color:#000;width:auto}.completions select option.context{color:#286090}#kernel_logo_widget{float:right!important;float:right}#kernel_logo_widget .current_kernel_logo{display:none;margin-top:-1px;margin-bottom:-1px;width:32px;height:32px}#menubar{box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box;margin-top:1px}#menubar .navbar{border-top:1px;border-radius:0 0 2px 2px;margin-bottom:0}#menubar .navbar-toggle{float:left;padding-top:7px;padding-bottom:7px;border:none}#menubar .navbar-collapse{clear:left}.nav-wrapper{border-bottom:1px solid #e7e7e7}i.menu-icon{padding-top:4px}ul#help_menu li a{overflow:hidden;padding-right:2.2em}ul#help_menu li a i{margin-right:-1.2em}.dropdown-submenu{position:relative}.dropdown-submenu>.dropdown-menu{top:0;left:100%;margin-top:-6px;margin-left:-1px}.dropdown-submenu:hover>.dropdown-menu{display:block}.dropdown-submenu>a:after{font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;display:block;content:"\f0da";float:right;color:#333;margin-top:2px;margin-right:-10px}.dropdown-submenu>a:after.pull-left{margin-right:.3em}.dropdown-submenu>a:after.pull-right{margin-left:.3em}.dropdown-submenu:hover>a:after{color:#262626}.dropdown-submenu.pull-left{float:none}.dropdown-submenu.pull-left>.dropdown-menu{left:-100%;margin-left:10px}#notification_area{float:right!important;float:right;z-index:10}.indicator_area{float:right!important;float:right;color:#777;margin-left:5px;margin-right:5px;z-index:10;text-align:center;width:auto}#kernel_indicator{float:right!important;float:right;color:#777;margin-left:5px;margin-right:5px;z-index:10;text-align:center;width:auto;border-left:1px solid}#kernel_indicator .kernel_indicator_name{padding-left:5px;padding-right:5px}#modal_indicator{float:right!important;float:right;color:#777;margin-left:5px;margin-right:5px;z-index:10;text-align:center;width:auto}#readonly-indicator{float:right!important;float:right;color:#777;z-index:10;text-align:center;width:auto;display:none;margin:2px 0 0}.modal_indicator:before{width:1.28571429em;text-align:center}.edit_mode .modal_indicator:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:"\f040"}.edit_mode .modal_indicator:before.pull-left{margin-right:.3em}.edit_mode .modal_indicator:before.pull-right{margin-left:.3em}.command_mode .modal_indicator:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:' '}.command_mode .modal_indicator:before.pull-left{margin-right:.3em}.command_mode .modal_indicator:before.pull-right{margin-left:.3em}.kernel_idle_icon:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:"\f10c"}.kernel_idle_icon:before.pull-left{margin-right:.3em}.kernel_idle_icon:before.pull-right{margin-left:.3em}.kernel_busy_icon:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:"\f111"}.kernel_busy_icon:before.pull-left{margin-right:.3em}.kernel_busy_icon:before.pull-right{margin-left:.3em}.kernel_dead_icon:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:"\f1e2"}.kernel_dead_icon:before.pull-left{margin-right:.3em}.kernel_dead_icon:before.pull-right{margin-left:.3em}.kernel_disconnected_icon:before{display:inline-block;font:normal normal normal 14px/1 FontAwesome;font-size:inherit;text-rendering:auto;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;content:"\f127"}.kernel_disconnected_icon:before.pull-left{margin-right:.3em}.kernel_disconnected_icon:before.pull-right{margin-left:.3em}.notification_widget{z-index:10;background:rgba(240,240,240,.5);margin-right:4px;color:#333;background-color:#fff;border-color:#ccc}.notification_widget.active,.notification_widget.focus,.notification_widget:active,.notification_widget:focus,.notification_widget:hover,.open>.dropdown-toggle.notification_widget{color:#333;background-color:#e6e6e6;border-color:#adadad}.notification_widget.active,.notification_widget:active,.open>.dropdown-toggle.notification_widget{background-image:none}.notification_widget.disabled,.notification_widget.disabled.active,.notification_widget.disabled.focus,.notification_widget.disabled:active,.notification_widget.disabled:focus,.notification_widget.disabled:hover,.notification_widget[disabled],.notification_widget[disabled].active,.notification_widget[disabled].focus,.notification_widget[disabled]:active,.notification_widget[disabled]:focus,.notification_widget[disabled]:hover,fieldset[disabled] .notification_widget,fieldset[disabled] .notification_widget.active,fieldset[disabled] .notification_widget.focus,fieldset[disabled] .notification_widget:active,fieldset[disabled] .notification_widget:focus,fieldset[disabled] .notification_widget:hover{background-color:#fff;border-color:#ccc}.notification_widget .badge{color:#fff;background-color:#333}.notification_widget.warning{color:#fff;background-color:#f0ad4e;border-color:#eea236}.notification_widget.warning.active,.notification_widget.warning.focus,.notification_widget.warning:active,.notification_widget.warning:focus,.notification_widget.warning:hover,.open>.dropdown-toggle.notification_widget.warning{color:#fff;background-color:#ec971f;border-color:#d58512}.notification_widget.warning.active,.notification_widget.warning:active,.open>.dropdown-toggle.notification_widget.warning{background-image:none}.notification_widget.warning.disabled,.notification_widget.warning.disabled.active,.notification_widget.warning.disabled.focus,.notification_widget.warning.disabled:active,.notification_widget.warning.disabled:focus,.notification_widget.warning.disabled:hover,.notification_widget.warning[disabled],.notification_widget.warning[disabled].active,.notification_widget.warning[disabled].focus,.notification_widget.warning[disabled]:active,.notification_widget.warning[disabled]:focus,.notification_widget.warning[disabled]:hover,fieldset[disabled] .notification_widget.warning,fieldset[disabled] .notification_widget.warning.active,fieldset[disabled] .notification_widget.warning.focus,fieldset[disabled] .notification_widget.warning:active,fieldset[disabled] .notification_widget.warning:focus,fieldset[disabled] .notification_widget.warning:hover{background-color:#f0ad4e;border-color:#eea236}.notification_widget.warning .badge{color:#f0ad4e;background-color:#fff}.notification_widget.success{color:#fff;background-color:#5cb85c;border-color:#4cae4c}.notification_widget.success.active,.notification_widget.success.focus,.notification_widget.success:active,.notification_widget.success:focus,.notification_widget.success:hover,.open>.dropdown-toggle.notification_widget.success{color:#fff;background-color:#449d44;border-color:#398439}.notification_widget.success.active,.notification_widget.success:active,.open>.dropdown-toggle.notification_widget.success{background-image:none}.notification_widget.success.disabled,.notification_widget.success.disabled.active,.notification_widget.success.disabled.focus,.notification_widget.success.disabled:active,.notification_widget.success.disabled:focus,.notification_widget.success.disabled:hover,.notification_widget.success[disabled],.notification_widget.success[disabled].active,.notification_widget.success[disabled].focus,.notification_widget.success[disabled]:active,.notification_widget.success[disabled]:focus,.notification_widget.success[disabled]:hover,fieldset[disabled] .notification_widget.success,fieldset[disabled] .notification_widget.success.active,fieldset[disabled] .notification_widget.success.focus,fieldset[disabled] .notification_widget.success:active,fieldset[disabled] .notification_widget.success:focus,fieldset[disabled] .notification_widget.success:hover{background-color:#5cb85c;border-color:#4cae4c}.notification_widget.success .badge{color:#5cb85c;background-color:#fff}.notification_widget.info{color:#fff;background-color:#5bc0de;border-color:#46b8da}.notification_widget.info.active,.notification_widget.info.focus,.notification_widget.info:active,.notification_widget.info:focus,.notification_widget.info:hover,.open>.dropdown-toggle.notification_widget.info{color:#fff;background-color:#31b0d5;border-color:#269abc}.notification_widget.info.active,.notification_widget.info:active,.open>.dropdown-toggle.notification_widget.info{background-image:none}.notification_widget.info.disabled,.notification_widget.info.disabled.active,.notification_widget.info.disabled.focus,.notification_widget.info.disabled:active,.notification_widget.info.disabled:focus,.notification_widget.info.disabled:hover,.notification_widget.info[disabled],.notification_widget.info[disabled].active,.notification_widget.info[disabled].focus,.notification_widget.info[disabled]:active,.notification_widget.info[disabled]:focus,.notification_widget.info[disabled]:hover,fieldset[disabled] .notification_widget.info,fieldset[disabled] .notification_widget.info.active,fieldset[disabled] .notification_widget.info.focus,fieldset[disabled] .notification_widget.info:active,fieldset[disabled] .notification_widget.info:focus,fieldset[disabled] .notification_widget.info:hover{background-color:#5bc0de;border-color:#46b8da}.notification_widget.info .badge{color:#5bc0de;background-color:#fff}.notification_widget.danger{color:#fff;background-color:#d9534f;border-color:#d43f3a}.notification_widget.danger.active,.notification_widget.danger.focus,.notification_widget.danger:active,.notification_widget.danger:focus,.notification_widget.danger:hover,.open>.dropdown-toggle.notification_widget.danger{color:#fff;background-color:#c9302c;border-color:#ac2925}.notification_widget.danger.active,.notification_widget.danger:active,.open>.dropdown-toggle.notification_widget.danger{background-image:none}.notification_widget.danger.disabled,.notification_widget.danger.disabled.active,.notification_widget.danger.disabled.focus,.notification_widget.danger.disabled:active,.notification_widget.danger.disabled:focus,.notification_widget.danger.disabled:hover,.notification_widget.danger[disabled],.notification_widget.danger[disabled].active,.notification_widget.danger[disabled].focus,.notification_widget.danger[disabled]:active,.notification_widget.danger[disabled]:focus,.notification_widget.danger[disabled]:hover,fieldset[disabled] .notification_widget.danger,fieldset[disabled] .notification_widget.danger.active,fieldset[disabled] .notification_widget.danger.focus,fieldset[disabled] .notification_widget.danger:active,fieldset[disabled] .notification_widget.danger:focus,fieldset[disabled] .notification_widget.danger:hover{background-color:#d9534f;border-color:#d43f3a}.notification_widget.danger .badge{color:#d9534f;background-color:#fff}div#pager{background-color:#fff;font-size:14px;line-height:20px;overflow:hidden;display:none;position:fixed;bottom:0;width:100%;max-height:50%;padding-top:8px;-webkit-box-shadow:0 0 12px 1px rgba(87,87,87,.2);box-shadow:0 0 12px 1px rgba(87,87,87,.2);z-index:100;top:auto!important}div#pager pre{line-height:1.21429em;color:#000;background-color:#f7f7f7;padding:.4em}div#pager #pager-button-area{position:absolute;top:8px;right:20px}div#pager #pager-contents{position:relative;overflow:auto;width:100%;height:100%}div#pager #pager-contents #pager-container{position:relative;padding:15px 0;box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box}div#pager .ui-resizable-handle{top:0;height:8px;background:#f7f7f7;border-top:1px solid #cfcfcf;border-bottom:1px solid #cfcfcf}div#pager .ui-resizable-handle::after{content:'';top:2px;left:50%;height:3px;width:30px;margin-left:-15px;position:absolute;border-top:1px solid #cfcfcf}.quickhelp{display:-webkit-box;-webkit-box-orient:horizontal;display:-moz-box;-moz-box-orient:horizontal;display:box;box-orient:horizontal;box-align:stretch;display:flex;flex-direction:row;align-items:stretch}.shortcut_key{display:inline-block;width:20ex;text-align:right;font-family:monospace}.shortcut_descr{display:inline-block;-webkit-box-flex:1;-moz-box-flex:1;box-flex:1;flex:1}span.save_widget{margin-top:6px}span.save_widget span.filename{height:1em;line-height:1em;padding:3px;margin-left:16px;border:none;font-size:146.5%;border-radius:2px}span.save_widget span.filename:hover{background-color:#e6e6e6}span.autosave_status,span.checkpoint_status{font-size:small}@media (max-width:767px){span.save_widget{font-size:small}span.autosave_status,span.checkpoint_status{display:none}}@media (min-width:768px)and (max-width:991px){span.checkpoint_status{display:none}span.autosave_status{font-size:x-small}}.toolbar{padding:0;margin-left:-5px;margin-top:2px;margin-bottom:5px;box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box}.toolbar label,.toolbar select{width:auto;vertical-align:middle;margin-bottom:0;display:inline;font-size:92%;margin-left:.3em;margin-right:.3em;padding:3px 0 0}.toolbar .btn{padding:2px 8px}.toolbar .btn-group{margin-top:0;margin-left:5px}#maintoolbar{margin-bottom:-3px;margin-top:-8px;border:0;min-height:27px;margin-left:0;padding-top:11px;padding-bottom:3px}#maintoolbar .navbar-text{float:none;vertical-align:middle;text-align:right;margin-left:5px;margin-right:0;margin-top:0}.select-xs{height:24px}@-moz-keyframes fadeOut{from{opacity:1}to{opacity:0}}@-webkit-keyframes fadeOut{from{opacity:1}to{opacity:0}}@-moz-keyframes fadeIn{from{opacity:0}to{opacity:1}}@-webkit-keyframes fadeIn{from{opacity:0}to{opacity:1}}.bigtooltip{overflow:auto;height:200px;-webkit-transition-property:height;-webkit-transition-duration:500ms;-moz-transition-property:height;-moz-transition-duration:500ms;transition-property:height;transition-duration:500ms}.smalltooltip{-webkit-transition-property:height;-webkit-transition-duration:500ms;-moz-transition-property:height;-moz-transition-duration:500ms;transition-property:height;transition-duration:500ms;text-overflow:ellipsis;overflow:hidden;height:80px}.tooltipbuttons{position:absolute;padding-right:15px;top:0;right:0}.tooltiptext{padding-right:30px}.ipython_tooltip{max-width:700px;animation:fadeOut 400ms;-webkit-animation:fadeIn 400ms;-moz-animation:fadeIn 400ms;animation:fadeIn 400ms;vertical-align:middle;background-color:#f7f7f7;overflow:visible;border:1px solid #ababab;outline:0;padding:3px 3px 3px 7px;padding-left:7px;font-family:monospace;min-height:50px;-moz-box-shadow:0 6px 10px -1px #adadad;-webkit-box-shadow:0 6px 10px -1px #adadad;box-shadow:0 6px 10px -1px #adadad;border-radius:2px;position:absolute;z-index:1000}.ipython_tooltip a{float:right}.ipython_tooltip .tooltiptext pre{border:0;border-radius:0;font-size:100%;background-color:#f7f7f7}.pretooltiparrow{left:0;margin:0;top:-16px;width:40px;height:16px;overflow:hidden;position:absolute}.pretooltiparrow:before{background-color:#f7f7f7;border:1px solid #ababab;z-index:11;content:"";position:absolute;left:15px;top:10px;width:25px;height:25px;-webkit-transform:rotate(45deg);-moz-transform:rotate(45deg);-ms-transform:rotate(45deg);-o-transform:rotate(45deg)}.terminal-app{background:#eee}.terminal-app #header{background:#fff;-webkit-box-shadow:0 0 12px 1px rgba(87,87,87,.2);box-shadow:0 0 12px 1px rgba(87,87,87,.2)}.terminal-app .terminal{float:left;font-family:monospace;color:#fff;background:#000;padding:.4em;border-radius:2px;-webkit-box-shadow:0 0 12px 1px rgba(87,87,87,.4);box-shadow:0 0 12px 1px rgba(87,87,87,.4)}.terminal-app .terminal,.terminal-app .terminal dummy-screen{line-height:1em;font-size:14px}.terminal-app .terminal-cursor{color:#000;background:#fff}.terminal-app #terminado-container{margin-top:20px}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}

@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="MSCI-719---Operations-Analytics---Case-Study-1">MSCI 719 - Operations Analytics - Case Study 1<a class="anchor-link" href="#MSCI-719---Operations-Analytics---Case-Study-1">&#182;</a></h1><h2 id="Rocket-Fuel:-Measuring-the-Effectiveness-of-Online-Advertising">Rocket Fuel: Measuring the Effectiveness of Online Advertising<a class="anchor-link" href="#Rocket-Fuel:-Measuring-the-Effectiveness-of-Online-Advertising">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Prepared by:</p>
<ul>
<li>Arif Hikmet Onat Balta - 20743281</li>
<li>Daniel Wei - 20498636</li>
<li>Sulaiman Olabiyi - 20690635</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="A.-Exploratory-Data-Analysis">A. Exploratory Data Analysis<a class="anchor-link" href="#A.-Exploratory-Data-Analysis">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>First, we need to import some necessary python modules and then read the csv data file.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># Import necessary modules</span>
<span class="kn">import</span> <span class="nn">scipy</span>
<span class="kn">from</span> <span class="nn">ggplot</span>  <span class="kn">import</span> <span class="o">*</span>
<span class="kn">import</span> <span class="nn">math</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="kn">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="kn">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="kn">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="kn">as</span> <span class="nn">plt</span>

<span class="o">%</span><span class="k">matplotlib</span> notebook
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># Import csv data as a pandas data frame (df)</span>
    
<span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s">&quot;Case1RocketFuel.csv&quot;</span><span class="p">,</span> <span class="n">sep</span><span class="o">=</span><span class="s">&#39;;&#39;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Second, we need to analyze each variable and check if there are any data set quirks.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 1. List variable names</span>

<span class="nb">list</span><span class="p">(</span><span class="n">df</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt output_prompt">Out[3]:</div>


<div class="output_text output_subarea output_execute_result">
<pre>[&apos;user_id&apos;, &apos;test&apos;, &apos;converted&apos;, &apos;tot_impr&apos;, &apos;mode_impr_day&apos;, &apos;mode_impr_hour&apos;]</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 2. List first few rows of data to understand more</span>

<span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">5</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt output_prompt">Out[4]:</div>

<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>user_id</th>
      <th>test</th>
      <th>converted</th>
      <th>tot_impr</th>
      <th>mode_impr_day</th>
      <th>mode_impr_hour</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1069124</td>
      <td>1</td>
      <td>0</td>
      <td>130</td>
      <td>1</td>
      <td>20</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1119715</td>
      <td>1</td>
      <td>0</td>
      <td>93</td>
      <td>2</td>
      <td>22</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1144181</td>
      <td>1</td>
      <td>0</td>
      <td>21</td>
      <td>2</td>
      <td>18</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1435133</td>
      <td>1</td>
      <td>0</td>
      <td>355</td>
      <td>2</td>
      <td>10</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1015700</td>
      <td>1</td>
      <td>0</td>
      <td>276</td>
      <td>5</td>
      <td>14</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 3. Check if each row has an unique user_id</span>

<span class="n">condition</span> <span class="o">=</span> <span class="nb">len</span><span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">user_id</span><span class="o">.</span><span class="n">unique</span><span class="p">())</span> <span class="o">==</span> <span class="n">df</span><span class="o">.</span><span class="n">user_id</span><span class="o">.</span><span class="n">count</span><span class="p">()</span>
<span class="k">print</span><span class="p">(</span><span class="s">&quot;Does each row has an unique user_id?: </span><span class="si">%s</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">condition</span>)
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Does each row has an unique user_id?: True
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 4. Check unique values of variables &#39;test&#39; and &#39;converted&#39; </span>

<span class="k">print</span><span class="p">(</span><span class="s">&quot;&#39;test&#39; column consists of these values: </span><span class="si">%s</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">df</span>.test.unique())
<span class="k">print</span><span class="p">(</span><span class="s">&quot;&#39;converted&#39; column consists of these values: </span><span class="si">%s</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">df</span>.converted.unique())
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>&apos;test&apos; column consists of these values: [1 0]
&apos;converted&apos; column consists of these values: [0 1]
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 5. Summarize last three variables</span>

<span class="k">print</span> <span class="s">&quot;Summarize &#39;tot_impr&#39;, &#39;mode_impr_day&#39; and &#39;mode_impr_hour&#39; columns: &quot;</span>
<span class="k">print</span> <span class="n">df</span><span class="p">[[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">,</span> <span class="s">&quot;mode_impr_day&quot;</span><span class="p">,</span> <span class="s">&quot;mode_impr_hour&quot;</span><span class="p">]]</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Summarize &apos;tot_impr&apos;, &apos;mode_impr_day&apos; and &apos;mode_impr_hour&apos; columns: 
            tot_impr  mode_impr_day  mode_impr_hour
count  588101.000000  588101.000000   588101.000000
mean       24.820876       4.025533       14.469061
std        43.715181       2.004019        4.834634
min         1.000000       1.000000        0.000000
25%         4.000000       2.000000       11.000000
50%        13.000000       4.000000       14.000000
75%        27.000000       6.000000       18.000000
max      2065.000000       7.000000       23.000000
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>'tot_impr' column ranges from 1 to 2065. This means some users are shown the online ad more than 2000 times.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 6. 99% percentile for &#39;tot_impr&#39;</span>

<span class="k">print</span><span class="p">(</span><span class="s">&quot;99</span><span class="si">%%</span><span class="s"> of impressions per user is between </span><span class="si">%d</span><span class="s"> and </span><span class="si">%d</span><span class="s">&quot;</span> <span class="o">%</span> <span class="p">(</span><span class="nb">min</span><span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">tot_impr</span><span class="p">),</span> <span class="n">df</span><span class="o">.</span><span class="n">tot_impr</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.99</span><span class="p">)))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>99% of impressions per user is between 1 and 202
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 7. PLot histogram of total impressions</span>

<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">tot_impr</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="s">&quot;auto&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s">&#39;Total Impressions&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s">&#39;Frequency&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s">&#39;Histogram of Total Impressions&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span> <span class="mi">202</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="mi">60000</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>


<div class="output_subarea output_javascript ">
<script type="text/javascript">
/* Put everything inside the global mpl namespace */
window.mpl = {};

mpl.get_websocket_type = function() {
    if (typeof(WebSocket) !== 'undefined') {
        return WebSocket;
    } else if (typeof(MozWebSocket) !== 'undefined') {
        return MozWebSocket;
    } else {
        alert('Your browser does not have WebSocket support.' +
              'Please try Chrome, Safari or Firefox ≥ 6. ' +
              'Firefox 4 and 5 are also supported but you ' +
              'have to enable WebSockets in about:config.');
    };
}

mpl.figure = function(figure_id, websocket, ondownload, parent_element) {
    this.id = figure_id;

    this.ws = websocket;

    this.supports_binary = (this.ws.binaryType != undefined);

    if (!this.supports_binary) {
        var warnings = document.getElementById("mpl-warnings");
        if (warnings) {
            warnings.style.display = 'block';
            warnings.textContent = (
                "This browser does not support binary websocket messages. " +
                    "Performance may be slow.");
        }
    }

    this.imageObj = new Image();

    this.context = undefined;
    this.message = undefined;
    this.canvas = undefined;
    this.rubberband_canvas = undefined;
    this.rubberband_context = undefined;
    this.format_dropdown = undefined;

    this.image_mode = 'full';

    this.root = $('<div/>');
    this._root_extra_style(this.root)
    this.root.attr('style', 'display: inline-block');

    $(parent_element).append(this.root);

    this._init_header(this);
    this._init_canvas(this);
    this._init_toolbar(this);

    var fig = this;

    this.waiting = false;

    this.ws.onopen =  function () {
            fig.send_message("supports_binary", {value: fig.supports_binary});
            fig.send_message("send_image_mode", {});
            fig.send_message("refresh", {});
        }

    this.imageObj.onload = function() {
            if (fig.image_mode == 'full') {
                // Full images could contain transparency (where diff images
                // almost always do), so we need to clear the canvas so that
                // there is no ghosting.
                fig.context.clearRect(0, 0, fig.canvas.width, fig.canvas.height);
            }
            fig.context.drawImage(fig.imageObj, 0, 0);
        };

    this.imageObj.onunload = function() {
        this.ws.close();
    }

    this.ws.onmessage = this._make_on_message_function(this);

    this.ondownload = ondownload;
}

mpl.figure.prototype._init_header = function() {
    var titlebar = $(
        '<div class="ui-dialog-titlebar ui-widget-header ui-corner-all ' +
        'ui-helper-clearfix"/>');
    var titletext = $(
        '<div class="ui-dialog-title" style="width: 100%; ' +
        'text-align: center; padding: 3px;"/>');
    titlebar.append(titletext)
    this.root.append(titlebar);
    this.header = titletext[0];
}



mpl.figure.prototype._canvas_extra_style = function(canvas_div) {

}


mpl.figure.prototype._root_extra_style = function(canvas_div) {

}

mpl.figure.prototype._init_canvas = function() {
    var fig = this;

    var canvas_div = $('<div/>');

    canvas_div.attr('style', 'position: relative; clear: both; outline: 0');

    function canvas_keyboard_event(event) {
        return fig.key_event(event, event['data']);
    }

    canvas_div.keydown('key_press', canvas_keyboard_event);
    canvas_div.keyup('key_release', canvas_keyboard_event);
    this.canvas_div = canvas_div
    this._canvas_extra_style(canvas_div)
    this.root.append(canvas_div);

    var canvas = $('<canvas/>');
    canvas.addClass('mpl-canvas');
    canvas.attr('style', "left: 0; top: 0; z-index: 0; outline: 0")

    this.canvas = canvas[0];
    this.context = canvas[0].getContext("2d");

    var rubberband = $('<canvas/>');
    rubberband.attr('style', "position: absolute; left: 0; top: 0; z-index: 1;")

    var pass_mouse_events = true;

    canvas_div.resizable({
        start: function(event, ui) {
            pass_mouse_events = false;
        },
        resize: function(event, ui) {
            fig.request_resize(ui.size.width, ui.size.height);
        },
        stop: function(event, ui) {
            pass_mouse_events = true;
            fig.request_resize(ui.size.width, ui.size.height);
        },
    });

    function mouse_event_fn(event) {
        if (pass_mouse_events)
            return fig.mouse_event(event, event['data']);
    }

    rubberband.mousedown('button_press', mouse_event_fn);
    rubberband.mouseup('button_release', mouse_event_fn);
    // Throttle sequential mouse events to 1 every 20ms.
    rubberband.mousemove('motion_notify', mouse_event_fn);

    rubberband.mouseenter('figure_enter', mouse_event_fn);
    rubberband.mouseleave('figure_leave', mouse_event_fn);

    canvas_div.on("wheel", function (event) {
        event = event.originalEvent;
        event['data'] = 'scroll'
        if (event.deltaY < 0) {
            event.step = 1;
        } else {
            event.step = -1;
        }
        mouse_event_fn(event);
    });

    canvas_div.append(canvas);
    canvas_div.append(rubberband);

    this.rubberband = rubberband;
    this.rubberband_canvas = rubberband[0];
    this.rubberband_context = rubberband[0].getContext("2d");
    this.rubberband_context.strokeStyle = "#000000";

    this._resize_canvas = function(width, height) {
        // Keep the size of the canvas, canvas container, and rubber band
        // canvas in synch.
        canvas_div.css('width', width)
        canvas_div.css('height', height)

        canvas.attr('width', width);
        canvas.attr('height', height);

        rubberband.attr('width', width);
        rubberband.attr('height', height);
    }

    // Set the figure to an initial 600x600px, this will subsequently be updated
    // upon first draw.
    this._resize_canvas(600, 600);

    // Disable right mouse context menu.
    $(this.rubberband_canvas).bind("contextmenu",function(e){
        return false;
    });

    function set_focus () {
        canvas.focus();
        canvas_div.focus();
    }

    window.setTimeout(set_focus, 100);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items) {
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) {
            // put a spacer in here.
            continue;
        }
        var button = $('<button/>');
        button.addClass('ui-button ui-widget ui-state-default ui-corner-all ' +
                        'ui-button-icon-only');
        button.attr('role', 'button');
        button.attr('aria-disabled', 'false');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);

        var icon_img = $('<span/>');
        icon_img.addClass('ui-button-icon-primary ui-icon');
        icon_img.addClass(image);
        icon_img.addClass('ui-corner-all');

        var tooltip_span = $('<span/>');
        tooltip_span.addClass('ui-button-text');
        tooltip_span.html(tooltip);

        button.append(icon_img);
        button.append(tooltip_span);

        nav_element.append(button);
    }

    var fmt_picker_span = $('<span/>');

    var fmt_picker = $('<select/>');
    fmt_picker.addClass('mpl-toolbar-option ui-widget ui-widget-content');
    fmt_picker_span.append(fmt_picker);
    nav_element.append(fmt_picker_span);
    this.format_dropdown = fmt_picker[0];

    for (var ind in mpl.extensions) {
        var fmt = mpl.extensions[ind];
        var option = $(
            '<option/>', {selected: fmt === mpl.default_extension}).html(fmt);
        fmt_picker.append(option)
    }

    // Add hover states to the ui-buttons
    $( ".ui-button" ).hover(
        function() { $(this).addClass("ui-state-hover");},
        function() { $(this).removeClass("ui-state-hover");}
    );

    var status_bar = $('<span class="mpl-message"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];
}

mpl.figure.prototype.request_resize = function(x_pixels, y_pixels) {
    // Request matplotlib to resize the figure. Matplotlib will then trigger a resize in the client,
    // which will in turn request a refresh of the image.
    this.send_message('resize', {'width': x_pixels, 'height': y_pixels});
}

mpl.figure.prototype.send_message = function(type, properties) {
    properties['type'] = type;
    properties['figure_id'] = this.id;
    this.ws.send(JSON.stringify(properties));
}

mpl.figure.prototype.send_draw_message = function() {
    if (!this.waiting) {
        this.waiting = true;
        this.ws.send(JSON.stringify({type: "draw", figure_id: this.id}));
    }
}


mpl.figure.prototype.handle_save = function(fig, msg) {
    var format_dropdown = fig.format_dropdown;
    var format = format_dropdown.options[format_dropdown.selectedIndex].value;
    fig.ondownload(fig, format);
}


mpl.figure.prototype.handle_resize = function(fig, msg) {
    var size = msg['size'];
    if (size[0] != fig.canvas.width || size[1] != fig.canvas.height) {
        fig._resize_canvas(size[0], size[1]);
        fig.send_message("refresh", {});
    };
}

mpl.figure.prototype.handle_rubberband = function(fig, msg) {
    var x0 = msg['x0'];
    var y0 = fig.canvas.height - msg['y0'];
    var x1 = msg['x1'];
    var y1 = fig.canvas.height - msg['y1'];
    x0 = Math.floor(x0) + 0.5;
    y0 = Math.floor(y0) + 0.5;
    x1 = Math.floor(x1) + 0.5;
    y1 = Math.floor(y1) + 0.5;
    var min_x = Math.min(x0, x1);
    var min_y = Math.min(y0, y1);
    var width = Math.abs(x1 - x0);
    var height = Math.abs(y1 - y0);

    fig.rubberband_context.clearRect(
        0, 0, fig.canvas.width, fig.canvas.height);

    fig.rubberband_context.strokeRect(min_x, min_y, width, height);
}

mpl.figure.prototype.handle_figure_label = function(fig, msg) {
    // Updates the figure title.
    fig.header.textContent = msg['label'];
}

mpl.figure.prototype.handle_cursor = function(fig, msg) {
    var cursor = msg['cursor'];
    switch(cursor)
    {
    case 0:
        cursor = 'pointer';
        break;
    case 1:
        cursor = 'default';
        break;
    case 2:
        cursor = 'crosshair';
        break;
    case 3:
        cursor = 'move';
        break;
    }
    fig.rubberband_canvas.style.cursor = cursor;
}

mpl.figure.prototype.handle_message = function(fig, msg) {
    fig.message.textContent = msg['message'];
}

mpl.figure.prototype.handle_draw = function(fig, msg) {
    // Request the server to send over a new figure.
    fig.send_draw_message();
}

mpl.figure.prototype.handle_image_mode = function(fig, msg) {
    fig.image_mode = msg['mode'];
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Called whenever the canvas gets updated.
    this.send_message("ack", {});
}

// A function to construct a web socket function for onmessage handling.
// Called in the figure constructor.
mpl.figure.prototype._make_on_message_function = function(fig) {
    return function socket_on_message(evt) {
        if (evt.data instanceof Blob) {
            /* FIXME: We get "Resource interpreted as Image but
             * transferred with MIME type text/plain:" errors on
             * Chrome.  But how to set the MIME type?  It doesn't seem
             * to be part of the websocket stream */
            evt.data.type = "image/png";

            /* Free the memory for the previous frames */
            if (fig.imageObj.src) {
                (window.URL || window.webkitURL).revokeObjectURL(
                    fig.imageObj.src);
            }

            fig.imageObj.src = (window.URL || window.webkitURL).createObjectURL(
                evt.data);
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }
        else if (typeof evt.data === 'string' && evt.data.slice(0, 21) == "data:image/png;base64") {
            fig.imageObj.src = evt.data;
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }

        var msg = JSON.parse(evt.data);
        var msg_type = msg['type'];

        // Call the  "handle_{type}" callback, which takes
        // the figure and JSON message as its only arguments.
        try {
            var callback = fig["handle_" + msg_type];
        } catch (e) {
            console.log("No handler for the '" + msg_type + "' message type: ", msg);
            return;
        }

        if (callback) {
            try {
                // console.log("Handling '" + msg_type + "' message: ", msg);
                callback(fig, msg);
            } catch (e) {
                console.log("Exception inside the 'handler_" + msg_type + "' callback:", e, e.stack, msg);
            }
        }
    };
}

// from http://stackoverflow.com/questions/1114465/getting-mouse-location-in-canvas
mpl.findpos = function(e) {
    //this section is from http://www.quirksmode.org/js/events_properties.html
    var targ;
    if (!e)
        e = window.event;
    if (e.target)
        targ = e.target;
    else if (e.srcElement)
        targ = e.srcElement;
    if (targ.nodeType == 3) // defeat Safari bug
        targ = targ.parentNode;

    // jQuery normalizes the pageX and pageY
    // pageX,Y are the mouse positions relative to the document
    // offset() returns the position of the element relative to the document
    var x = e.pageX - $(targ).offset().left;
    var y = e.pageY - $(targ).offset().top;

    return {"x": x, "y": y};
};

/*
 * return a copy of an object with only non-object keys
 * we need this to avoid circular references
 * http://stackoverflow.com/a/24161582/3208463
 */
function simpleKeys (original) {
  return Object.keys(original).reduce(function (obj, key) {
    if (typeof original[key] !== 'object')
        obj[key] = original[key]
    return obj;
  }, {});
}

mpl.figure.prototype.mouse_event = function(event, name) {
    var canvas_pos = mpl.findpos(event)

    if (name === 'button_press')
    {
        this.canvas.focus();
        this.canvas_div.focus();
    }

    var x = canvas_pos.x;
    var y = canvas_pos.y;

    this.send_message(name, {x: x, y: y, button: event.button,
                             step: event.step,
                             guiEvent: simpleKeys(event)});

    /* This prevents the web browser from automatically changing to
     * the text insertion cursor when the button is pressed.  We want
     * to control all of the cursor setting manually through the
     * 'cursor' event from matplotlib */
    event.preventDefault();
    return false;
}

mpl.figure.prototype._key_event_extra = function(event, name) {
    // Handle any extra behaviour associated with a key event
}

mpl.figure.prototype.key_event = function(event, name) {

    // Prevent repeat events
    if (name == 'key_press')
    {
        if (event.which === this._key)
            return;
        else
            this._key = event.which;
    }
    if (name == 'key_release')
        this._key = null;

    var value = '';
    if (event.ctrlKey && event.which != 17)
        value += "ctrl+";
    if (event.altKey && event.which != 18)
        value += "alt+";
    if (event.shiftKey && event.which != 16)
        value += "shift+";

    value += 'k';
    value += event.which.toString();

    this._key_event_extra(event, name);

    this.send_message(name, {key: value,
                             guiEvent: simpleKeys(event)});
    return false;
}

mpl.figure.prototype.toolbar_button_onclick = function(name) {
    if (name == 'download') {
        this.handle_save(this, null);
    } else {
        this.send_message("toolbar_button", {name: name});
    }
};

mpl.figure.prototype.toolbar_button_onmouseover = function(tooltip) {
    this.message.textContent = tooltip;
};
mpl.toolbar_items = [["Home", "Reset original view", "fa fa-home icon-home", "home"], ["Back", "Back to  previous view", "fa fa-arrow-left icon-arrow-left", "back"], ["Forward", "Forward to next view", "fa fa-arrow-right icon-arrow-right", "forward"], ["", "", "", ""], ["Pan", "Pan axes with left mouse, zoom with right", "fa fa-arrows icon-move", "pan"], ["Zoom", "Zoom to rectangle", "fa fa-square-o icon-check-empty", "zoom"], ["", "", "", ""], ["Download", "Download plot", "fa fa-floppy-o icon-save", "download"]];

mpl.extensions = ["eps", "jpeg", "pdf", "png", "ps", "raw", "svg", "tif"];

mpl.default_extension = "png";var comm_websocket_adapter = function(comm) {
    // Create a "websocket"-like object which calls the given IPython comm
    // object with the appropriate methods. Currently this is a non binary
    // socket, so there is still some room for performance tuning.
    var ws = {};

    ws.close = function() {
        comm.close()
    };
    ws.send = function(m) {
        //console.log('sending', m);
        comm.send(m);
    };
    // Register the callback with on_msg.
    comm.on_msg(function(msg) {
        //console.log('receiving', msg['content']['data'], msg);
        // Pass the mpl event to the overriden (by mpl) onmessage function.
        ws.onmessage(msg['content']['data'])
    });
    return ws;
}

mpl.mpl_figure_comm = function(comm, msg) {
    // This is the function which gets called when the mpl process
    // starts-up an IPython Comm through the "matplotlib" channel.

    var id = msg.content.data.id;
    // Get hold of the div created by the display call when the Comm
    // socket was opened in Python.
    var element = $("#" + id);
    var ws_proxy = comm_websocket_adapter(comm)

    function ondownload(figure, format) {
        window.open(figure.imageObj.src);
    }

    var fig = new mpl.figure(id, ws_proxy,
                           ondownload,
                           element.get(0));

    // Call onopen now - mpl needs it, as it is assuming we've passed it a real
    // web socket which is closed, not our websocket->open comm proxy.
    ws_proxy.onopen();

    fig.parent_element = element.get(0);
    fig.cell_info = mpl.find_output_cell("<div id='" + id + "'></div>");
    if (!fig.cell_info) {
        console.error("Failed to find cell for figure", id, fig);
        return;
    }

    var output_index = fig.cell_info[2]
    var cell = fig.cell_info[0];

};

mpl.figure.prototype.handle_close = function(fig, msg) {
    fig.root.unbind('remove')

    // Update the output cell to use the data from the current canvas.
    fig.push_to_output();
    var dataURL = fig.canvas.toDataURL();
    // Re-enable the keyboard manager in IPython - without this line, in FF,
    // the notebook keyboard shortcuts fail.
    IPython.keyboard_manager.enable()
    $(fig.parent_element).html('<img src="' + dataURL + '">');
    fig.close_ws(fig, msg);
}

mpl.figure.prototype.close_ws = function(fig, msg){
    fig.send_message('closing', msg);
    // fig.ws.close()
}

mpl.figure.prototype.push_to_output = function(remove_interactive) {
    // Turn the data on the canvas into data in the output cell.
    var dataURL = this.canvas.toDataURL();
    this.cell_info[1]['text/html'] = '<img src="' + dataURL + '">';
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Tell IPython that the notebook contents must change.
    IPython.notebook.set_dirty(true);
    this.send_message("ack", {});
    var fig = this;
    // Wait a second, then push the new image to the DOM so
    // that it is saved nicely (might be nice to debounce this).
    setTimeout(function () { fig.push_to_output() }, 1000);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items){
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) { continue; };

        var button = $('<button class="btn btn-default" href="#" title="' + name + '"><i class="fa ' + image + ' fa-lg"></i></button>');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);
        nav_element.append(button);
    }

    // Add the status bar.
    var status_bar = $('<span class="mpl-message" style="text-align:right; float: right;"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];

    // Add the close button to the window.
    var buttongrp = $('<div class="btn-group inline pull-right"></div>');
    var button = $('<button class="btn btn-mini btn-primary" href="#" title="Stop Interaction"><i class="fa fa-power-off icon-remove icon-large"></i></button>');
    button.click(function (evt) { fig.handle_close(fig, {}); } );
    button.mouseover('Stop Interaction', toolbar_mouse_event);
    buttongrp.append(button);
    var titlebar = this.root.find($('.ui-dialog-titlebar'));
    titlebar.prepend(buttongrp);
}

mpl.figure.prototype._root_extra_style = function(el){
    var fig = this
    el.on("remove", function(){
	fig.close_ws(fig, {});
    });
}

mpl.figure.prototype._canvas_extra_style = function(el){
    // this is important to make the div 'focusable
    el.attr('tabindex', 0)
    // reach out to IPython and tell the keyboard manager to turn it's self
    // off when our div gets focus

    // location in version 3
    if (IPython.notebook.keyboard_manager) {
        IPython.notebook.keyboard_manager.register_events(el);
    }
    else {
        // location in version 2
        IPython.keyboard_manager.register_events(el);
    }

}

mpl.figure.prototype._key_event_extra = function(event, name) {
    var manager = IPython.notebook.keyboard_manager;
    if (!manager)
        manager = IPython.keyboard_manager;

    // Check for shift+enter
    if (event.shiftKey && event.which == 13) {
        this.canvas_div.blur();
        event.shiftKey = false;
        // Send a "J" for go to next cell
        event.which = 74;
        event.keyCode = 74;
        manager.command_mode();
        manager.handle_keydown(event);
    }
}

mpl.figure.prototype.handle_save = function(fig, msg) {
    fig.ondownload(fig, null);
}


mpl.find_output_cell = function(html_output) {
    // Return the cell and output element which can be found *uniquely* in the notebook.
    // Note - this is a bit hacky, but it is done because the "notebook_saving.Notebook"
    // IPython event is triggered only after the cells have been serialised, which for
    // our purposes (turning an active figure into a static one), is too late.
    var cells = IPython.notebook.get_cells();
    var ncells = cells.length;
    for (var i=0; i<ncells; i++) {
        var cell = cells[i];
        if (cell.cell_type === 'code'){
            for (var j=0; j<cell.output_area.outputs.length; j++) {
                var data = cell.output_area.outputs[j];
                if (data.data) {
                    // IPython >= 3 moved mimebundle to data attribute of output
                    data = data.data;
                }
                if (data['text/html'] == html_output) {
                    return [cell, data, j];
                }
            }
        }
    }
}

// Register the function which deals with the matplotlib target/channel.
// The kernel may be null if the page has been refreshed.
if (IPython.notebook.kernel != null) {
    IPython.notebook.kernel.comm_manager.register_target('matplotlib', mpl.mpl_figure_comm);
}

</script>
</div>

</div>

<div class="output_area"><div class="prompt"></div>

<div class="output_html rendered_html output_subarea ">
<img src="data:image/png;base64,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">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>It looks like 'tot_impr' column has a poisson distribution with a very long tail on the right.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 8. Who saw the advertisement more? Converted or non-converted users?</span>

<span class="k">print</span><span class="p">(</span><span class="s">&quot;Average impression of converted users: </span><span class="si">%d</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">df</span>[&quot;tot_impr&quot;][df[&quot;converted&quot;]==1].mean())
<span class="k">print</span><span class="p">(</span><span class="s">&quot;Average impression of non-converted users: </span><span class="si">%d</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">df</span>[&quot;tot_impr&quot;][df[&quot;converted&quot;]==0].mean())

<span class="k">print</span><span class="p">(</span><span class="s">&quot;Median impression of converted users: </span><span class="si">%d</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">df</span>[&quot;tot_impr&quot;][df[&quot;converted&quot;]==1].median())
<span class="k">print</span><span class="p">(</span><span class="s">&quot;Median impression of non-converted users: </span><span class="si">%d</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">df</span>[&quot;tot_impr&quot;][df[&quot;converted&quot;]==0].median())
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Average impression of converted users: 83
Average impression of non-converted users: 23
Median impression of converted users: 64
Median impression of non-converted users: 13
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 9. Plot histogram of impressions for converted test-group users</span>

<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">df</span><span class="p">[(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)][</span><span class="s">&quot;tot_impr&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">values</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="mi">300</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s">&#39;Total Impressions&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s">&#39;Frequency&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s">&#39;Histogram of Total Impressions For Converted Test Group&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span> <span class="mi">600</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="mi">900</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>


<div class="output_subarea output_javascript ">
<script type="text/javascript">
/* Put everything inside the global mpl namespace */
window.mpl = {};

mpl.get_websocket_type = function() {
    if (typeof(WebSocket) !== 'undefined') {
        return WebSocket;
    } else if (typeof(MozWebSocket) !== 'undefined') {
        return MozWebSocket;
    } else {
        alert('Your browser does not have WebSocket support.' +
              'Please try Chrome, Safari or Firefox ≥ 6. ' +
              'Firefox 4 and 5 are also supported but you ' +
              'have to enable WebSockets in about:config.');
    };
}

mpl.figure = function(figure_id, websocket, ondownload, parent_element) {
    this.id = figure_id;

    this.ws = websocket;

    this.supports_binary = (this.ws.binaryType != undefined);

    if (!this.supports_binary) {
        var warnings = document.getElementById("mpl-warnings");
        if (warnings) {
            warnings.style.display = 'block';
            warnings.textContent = (
                "This browser does not support binary websocket messages. " +
                    "Performance may be slow.");
        }
    }

    this.imageObj = new Image();

    this.context = undefined;
    this.message = undefined;
    this.canvas = undefined;
    this.rubberband_canvas = undefined;
    this.rubberband_context = undefined;
    this.format_dropdown = undefined;

    this.image_mode = 'full';

    this.root = $('<div/>');
    this._root_extra_style(this.root)
    this.root.attr('style', 'display: inline-block');

    $(parent_element).append(this.root);

    this._init_header(this);
    this._init_canvas(this);
    this._init_toolbar(this);

    var fig = this;

    this.waiting = false;

    this.ws.onopen =  function () {
            fig.send_message("supports_binary", {value: fig.supports_binary});
            fig.send_message("send_image_mode", {});
            fig.send_message("refresh", {});
        }

    this.imageObj.onload = function() {
            if (fig.image_mode == 'full') {
                // Full images could contain transparency (where diff images
                // almost always do), so we need to clear the canvas so that
                // there is no ghosting.
                fig.context.clearRect(0, 0, fig.canvas.width, fig.canvas.height);
            }
            fig.context.drawImage(fig.imageObj, 0, 0);
        };

    this.imageObj.onunload = function() {
        this.ws.close();
    }

    this.ws.onmessage = this._make_on_message_function(this);

    this.ondownload = ondownload;
}

mpl.figure.prototype._init_header = function() {
    var titlebar = $(
        '<div class="ui-dialog-titlebar ui-widget-header ui-corner-all ' +
        'ui-helper-clearfix"/>');
    var titletext = $(
        '<div class="ui-dialog-title" style="width: 100%; ' +
        'text-align: center; padding: 3px;"/>');
    titlebar.append(titletext)
    this.root.append(titlebar);
    this.header = titletext[0];
}



mpl.figure.prototype._canvas_extra_style = function(canvas_div) {

}


mpl.figure.prototype._root_extra_style = function(canvas_div) {

}

mpl.figure.prototype._init_canvas = function() {
    var fig = this;

    var canvas_div = $('<div/>');

    canvas_div.attr('style', 'position: relative; clear: both; outline: 0');

    function canvas_keyboard_event(event) {
        return fig.key_event(event, event['data']);
    }

    canvas_div.keydown('key_press', canvas_keyboard_event);
    canvas_div.keyup('key_release', canvas_keyboard_event);
    this.canvas_div = canvas_div
    this._canvas_extra_style(canvas_div)
    this.root.append(canvas_div);

    var canvas = $('<canvas/>');
    canvas.addClass('mpl-canvas');
    canvas.attr('style', "left: 0; top: 0; z-index: 0; outline: 0")

    this.canvas = canvas[0];
    this.context = canvas[0].getContext("2d");

    var rubberband = $('<canvas/>');
    rubberband.attr('style', "position: absolute; left: 0; top: 0; z-index: 1;")

    var pass_mouse_events = true;

    canvas_div.resizable({
        start: function(event, ui) {
            pass_mouse_events = false;
        },
        resize: function(event, ui) {
            fig.request_resize(ui.size.width, ui.size.height);
        },
        stop: function(event, ui) {
            pass_mouse_events = true;
            fig.request_resize(ui.size.width, ui.size.height);
        },
    });

    function mouse_event_fn(event) {
        if (pass_mouse_events)
            return fig.mouse_event(event, event['data']);
    }

    rubberband.mousedown('button_press', mouse_event_fn);
    rubberband.mouseup('button_release', mouse_event_fn);
    // Throttle sequential mouse events to 1 every 20ms.
    rubberband.mousemove('motion_notify', mouse_event_fn);

    rubberband.mouseenter('figure_enter', mouse_event_fn);
    rubberband.mouseleave('figure_leave', mouse_event_fn);

    canvas_div.on("wheel", function (event) {
        event = event.originalEvent;
        event['data'] = 'scroll'
        if (event.deltaY < 0) {
            event.step = 1;
        } else {
            event.step = -1;
        }
        mouse_event_fn(event);
    });

    canvas_div.append(canvas);
    canvas_div.append(rubberband);

    this.rubberband = rubberband;
    this.rubberband_canvas = rubberband[0];
    this.rubberband_context = rubberband[0].getContext("2d");
    this.rubberband_context.strokeStyle = "#000000";

    this._resize_canvas = function(width, height) {
        // Keep the size of the canvas, canvas container, and rubber band
        // canvas in synch.
        canvas_div.css('width', width)
        canvas_div.css('height', height)

        canvas.attr('width', width);
        canvas.attr('height', height);

        rubberband.attr('width', width);
        rubberband.attr('height', height);
    }

    // Set the figure to an initial 600x600px, this will subsequently be updated
    // upon first draw.
    this._resize_canvas(600, 600);

    // Disable right mouse context menu.
    $(this.rubberband_canvas).bind("contextmenu",function(e){
        return false;
    });

    function set_focus () {
        canvas.focus();
        canvas_div.focus();
    }

    window.setTimeout(set_focus, 100);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items) {
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) {
            // put a spacer in here.
            continue;
        }
        var button = $('<button/>');
        button.addClass('ui-button ui-widget ui-state-default ui-corner-all ' +
                        'ui-button-icon-only');
        button.attr('role', 'button');
        button.attr('aria-disabled', 'false');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);

        var icon_img = $('<span/>');
        icon_img.addClass('ui-button-icon-primary ui-icon');
        icon_img.addClass(image);
        icon_img.addClass('ui-corner-all');

        var tooltip_span = $('<span/>');
        tooltip_span.addClass('ui-button-text');
        tooltip_span.html(tooltip);

        button.append(icon_img);
        button.append(tooltip_span);

        nav_element.append(button);
    }

    var fmt_picker_span = $('<span/>');

    var fmt_picker = $('<select/>');
    fmt_picker.addClass('mpl-toolbar-option ui-widget ui-widget-content');
    fmt_picker_span.append(fmt_picker);
    nav_element.append(fmt_picker_span);
    this.format_dropdown = fmt_picker[0];

    for (var ind in mpl.extensions) {
        var fmt = mpl.extensions[ind];
        var option = $(
            '<option/>', {selected: fmt === mpl.default_extension}).html(fmt);
        fmt_picker.append(option)
    }

    // Add hover states to the ui-buttons
    $( ".ui-button" ).hover(
        function() { $(this).addClass("ui-state-hover");},
        function() { $(this).removeClass("ui-state-hover");}
    );

    var status_bar = $('<span class="mpl-message"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];
}

mpl.figure.prototype.request_resize = function(x_pixels, y_pixels) {
    // Request matplotlib to resize the figure. Matplotlib will then trigger a resize in the client,
    // which will in turn request a refresh of the image.
    this.send_message('resize', {'width': x_pixels, 'height': y_pixels});
}

mpl.figure.prototype.send_message = function(type, properties) {
    properties['type'] = type;
    properties['figure_id'] = this.id;
    this.ws.send(JSON.stringify(properties));
}

mpl.figure.prototype.send_draw_message = function() {
    if (!this.waiting) {
        this.waiting = true;
        this.ws.send(JSON.stringify({type: "draw", figure_id: this.id}));
    }
}


mpl.figure.prototype.handle_save = function(fig, msg) {
    var format_dropdown = fig.format_dropdown;
    var format = format_dropdown.options[format_dropdown.selectedIndex].value;
    fig.ondownload(fig, format);
}


mpl.figure.prototype.handle_resize = function(fig, msg) {
    var size = msg['size'];
    if (size[0] != fig.canvas.width || size[1] != fig.canvas.height) {
        fig._resize_canvas(size[0], size[1]);
        fig.send_message("refresh", {});
    };
}

mpl.figure.prototype.handle_rubberband = function(fig, msg) {
    var x0 = msg['x0'];
    var y0 = fig.canvas.height - msg['y0'];
    var x1 = msg['x1'];
    var y1 = fig.canvas.height - msg['y1'];
    x0 = Math.floor(x0) + 0.5;
    y0 = Math.floor(y0) + 0.5;
    x1 = Math.floor(x1) + 0.5;
    y1 = Math.floor(y1) + 0.5;
    var min_x = Math.min(x0, x1);
    var min_y = Math.min(y0, y1);
    var width = Math.abs(x1 - x0);
    var height = Math.abs(y1 - y0);

    fig.rubberband_context.clearRect(
        0, 0, fig.canvas.width, fig.canvas.height);

    fig.rubberband_context.strokeRect(min_x, min_y, width, height);
}

mpl.figure.prototype.handle_figure_label = function(fig, msg) {
    // Updates the figure title.
    fig.header.textContent = msg['label'];
}

mpl.figure.prototype.handle_cursor = function(fig, msg) {
    var cursor = msg['cursor'];
    switch(cursor)
    {
    case 0:
        cursor = 'pointer';
        break;
    case 1:
        cursor = 'default';
        break;
    case 2:
        cursor = 'crosshair';
        break;
    case 3:
        cursor = 'move';
        break;
    }
    fig.rubberband_canvas.style.cursor = cursor;
}

mpl.figure.prototype.handle_message = function(fig, msg) {
    fig.message.textContent = msg['message'];
}

mpl.figure.prototype.handle_draw = function(fig, msg) {
    // Request the server to send over a new figure.
    fig.send_draw_message();
}

mpl.figure.prototype.handle_image_mode = function(fig, msg) {
    fig.image_mode = msg['mode'];
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Called whenever the canvas gets updated.
    this.send_message("ack", {});
}

// A function to construct a web socket function for onmessage handling.
// Called in the figure constructor.
mpl.figure.prototype._make_on_message_function = function(fig) {
    return function socket_on_message(evt) {
        if (evt.data instanceof Blob) {
            /* FIXME: We get "Resource interpreted as Image but
             * transferred with MIME type text/plain:" errors on
             * Chrome.  But how to set the MIME type?  It doesn't seem
             * to be part of the websocket stream */
            evt.data.type = "image/png";

            /* Free the memory for the previous frames */
            if (fig.imageObj.src) {
                (window.URL || window.webkitURL).revokeObjectURL(
                    fig.imageObj.src);
            }

            fig.imageObj.src = (window.URL || window.webkitURL).createObjectURL(
                evt.data);
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }
        else if (typeof evt.data === 'string' && evt.data.slice(0, 21) == "data:image/png;base64") {
            fig.imageObj.src = evt.data;
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }

        var msg = JSON.parse(evt.data);
        var msg_type = msg['type'];

        // Call the  "handle_{type}" callback, which takes
        // the figure and JSON message as its only arguments.
        try {
            var callback = fig["handle_" + msg_type];
        } catch (e) {
            console.log("No handler for the '" + msg_type + "' message type: ", msg);
            return;
        }

        if (callback) {
            try {
                // console.log("Handling '" + msg_type + "' message: ", msg);
                callback(fig, msg);
            } catch (e) {
                console.log("Exception inside the 'handler_" + msg_type + "' callback:", e, e.stack, msg);
            }
        }
    };
}

// from http://stackoverflow.com/questions/1114465/getting-mouse-location-in-canvas
mpl.findpos = function(e) {
    //this section is from http://www.quirksmode.org/js/events_properties.html
    var targ;
    if (!e)
        e = window.event;
    if (e.target)
        targ = e.target;
    else if (e.srcElement)
        targ = e.srcElement;
    if (targ.nodeType == 3) // defeat Safari bug
        targ = targ.parentNode;

    // jQuery normalizes the pageX and pageY
    // pageX,Y are the mouse positions relative to the document
    // offset() returns the position of the element relative to the document
    var x = e.pageX - $(targ).offset().left;
    var y = e.pageY - $(targ).offset().top;

    return {"x": x, "y": y};
};

/*
 * return a copy of an object with only non-object keys
 * we need this to avoid circular references
 * http://stackoverflow.com/a/24161582/3208463
 */
function simpleKeys (original) {
  return Object.keys(original).reduce(function (obj, key) {
    if (typeof original[key] !== 'object')
        obj[key] = original[key]
    return obj;
  }, {});
}

mpl.figure.prototype.mouse_event = function(event, name) {
    var canvas_pos = mpl.findpos(event)

    if (name === 'button_press')
    {
        this.canvas.focus();
        this.canvas_div.focus();
    }

    var x = canvas_pos.x;
    var y = canvas_pos.y;

    this.send_message(name, {x: x, y: y, button: event.button,
                             step: event.step,
                             guiEvent: simpleKeys(event)});

    /* This prevents the web browser from automatically changing to
     * the text insertion cursor when the button is pressed.  We want
     * to control all of the cursor setting manually through the
     * 'cursor' event from matplotlib */
    event.preventDefault();
    return false;
}

mpl.figure.prototype._key_event_extra = function(event, name) {
    // Handle any extra behaviour associated with a key event
}

mpl.figure.prototype.key_event = function(event, name) {

    // Prevent repeat events
    if (name == 'key_press')
    {
        if (event.which === this._key)
            return;
        else
            this._key = event.which;
    }
    if (name == 'key_release')
        this._key = null;

    var value = '';
    if (event.ctrlKey && event.which != 17)
        value += "ctrl+";
    if (event.altKey && event.which != 18)
        value += "alt+";
    if (event.shiftKey && event.which != 16)
        value += "shift+";

    value += 'k';
    value += event.which.toString();

    this._key_event_extra(event, name);

    this.send_message(name, {key: value,
                             guiEvent: simpleKeys(event)});
    return false;
}

mpl.figure.prototype.toolbar_button_onclick = function(name) {
    if (name == 'download') {
        this.handle_save(this, null);
    } else {
        this.send_message("toolbar_button", {name: name});
    }
};

mpl.figure.prototype.toolbar_button_onmouseover = function(tooltip) {
    this.message.textContent = tooltip;
};
mpl.toolbar_items = [["Home", "Reset original view", "fa fa-home icon-home", "home"], ["Back", "Back to  previous view", "fa fa-arrow-left icon-arrow-left", "back"], ["Forward", "Forward to next view", "fa fa-arrow-right icon-arrow-right", "forward"], ["", "", "", ""], ["Pan", "Pan axes with left mouse, zoom with right", "fa fa-arrows icon-move", "pan"], ["Zoom", "Zoom to rectangle", "fa fa-square-o icon-check-empty", "zoom"], ["", "", "", ""], ["Download", "Download plot", "fa fa-floppy-o icon-save", "download"]];

mpl.extensions = ["eps", "jpeg", "pdf", "png", "ps", "raw", "svg", "tif"];

mpl.default_extension = "png";var comm_websocket_adapter = function(comm) {
    // Create a "websocket"-like object which calls the given IPython comm
    // object with the appropriate methods. Currently this is a non binary
    // socket, so there is still some room for performance tuning.
    var ws = {};

    ws.close = function() {
        comm.close()
    };
    ws.send = function(m) {
        //console.log('sending', m);
        comm.send(m);
    };
    // Register the callback with on_msg.
    comm.on_msg(function(msg) {
        //console.log('receiving', msg['content']['data'], msg);
        // Pass the mpl event to the overriden (by mpl) onmessage function.
        ws.onmessage(msg['content']['data'])
    });
    return ws;
}

mpl.mpl_figure_comm = function(comm, msg) {
    // This is the function which gets called when the mpl process
    // starts-up an IPython Comm through the "matplotlib" channel.

    var id = msg.content.data.id;
    // Get hold of the div created by the display call when the Comm
    // socket was opened in Python.
    var element = $("#" + id);
    var ws_proxy = comm_websocket_adapter(comm)

    function ondownload(figure, format) {
        window.open(figure.imageObj.src);
    }

    var fig = new mpl.figure(id, ws_proxy,
                           ondownload,
                           element.get(0));

    // Call onopen now - mpl needs it, as it is assuming we've passed it a real
    // web socket which is closed, not our websocket->open comm proxy.
    ws_proxy.onopen();

    fig.parent_element = element.get(0);
    fig.cell_info = mpl.find_output_cell("<div id='" + id + "'></div>");
    if (!fig.cell_info) {
        console.error("Failed to find cell for figure", id, fig);
        return;
    }

    var output_index = fig.cell_info[2]
    var cell = fig.cell_info[0];

};

mpl.figure.prototype.handle_close = function(fig, msg) {
    fig.root.unbind('remove')

    // Update the output cell to use the data from the current canvas.
    fig.push_to_output();
    var dataURL = fig.canvas.toDataURL();
    // Re-enable the keyboard manager in IPython - without this line, in FF,
    // the notebook keyboard shortcuts fail.
    IPython.keyboard_manager.enable()
    $(fig.parent_element).html('<img src="' + dataURL + '">');
    fig.close_ws(fig, msg);
}

mpl.figure.prototype.close_ws = function(fig, msg){
    fig.send_message('closing', msg);
    // fig.ws.close()
}

mpl.figure.prototype.push_to_output = function(remove_interactive) {
    // Turn the data on the canvas into data in the output cell.
    var dataURL = this.canvas.toDataURL();
    this.cell_info[1]['text/html'] = '<img src="' + dataURL + '">';
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Tell IPython that the notebook contents must change.
    IPython.notebook.set_dirty(true);
    this.send_message("ack", {});
    var fig = this;
    // Wait a second, then push the new image to the DOM so
    // that it is saved nicely (might be nice to debounce this).
    setTimeout(function () { fig.push_to_output() }, 1000);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items){
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) { continue; };

        var button = $('<button class="btn btn-default" href="#" title="' + name + '"><i class="fa ' + image + ' fa-lg"></i></button>');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);
        nav_element.append(button);
    }

    // Add the status bar.
    var status_bar = $('<span class="mpl-message" style="text-align:right; float: right;"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];

    // Add the close button to the window.
    var buttongrp = $('<div class="btn-group inline pull-right"></div>');
    var button = $('<button class="btn btn-mini btn-primary" href="#" title="Stop Interaction"><i class="fa fa-power-off icon-remove icon-large"></i></button>');
    button.click(function (evt) { fig.handle_close(fig, {}); } );
    button.mouseover('Stop Interaction', toolbar_mouse_event);
    buttongrp.append(button);
    var titlebar = this.root.find($('.ui-dialog-titlebar'));
    titlebar.prepend(buttongrp);
}

mpl.figure.prototype._root_extra_style = function(el){
    var fig = this
    el.on("remove", function(){
	fig.close_ws(fig, {});
    });
}

mpl.figure.prototype._canvas_extra_style = function(el){
    // this is important to make the div 'focusable
    el.attr('tabindex', 0)
    // reach out to IPython and tell the keyboard manager to turn it's self
    // off when our div gets focus

    // location in version 3
    if (IPython.notebook.keyboard_manager) {
        IPython.notebook.keyboard_manager.register_events(el);
    }
    else {
        // location in version 2
        IPython.keyboard_manager.register_events(el);
    }

}

mpl.figure.prototype._key_event_extra = function(event, name) {
    var manager = IPython.notebook.keyboard_manager;
    if (!manager)
        manager = IPython.keyboard_manager;

    // Check for shift+enter
    if (event.shiftKey && event.which == 13) {
        this.canvas_div.blur();
        event.shiftKey = false;
        // Send a "J" for go to next cell
        event.which = 74;
        event.keyCode = 74;
        manager.command_mode();
        manager.handle_keydown(event);
    }
}

mpl.figure.prototype.handle_save = function(fig, msg) {
    fig.ondownload(fig, null);
}


mpl.find_output_cell = function(html_output) {
    // Return the cell and output element which can be found *uniquely* in the notebook.
    // Note - this is a bit hacky, but it is done because the "notebook_saving.Notebook"
    // IPython event is triggered only after the cells have been serialised, which for
    // our purposes (turning an active figure into a static one), is too late.
    var cells = IPython.notebook.get_cells();
    var ncells = cells.length;
    for (var i=0; i<ncells; i++) {
        var cell = cells[i];
        if (cell.cell_type === 'code'){
            for (var j=0; j<cell.output_area.outputs.length; j++) {
                var data = cell.output_area.outputs[j];
                if (data.data) {
                    // IPython >= 3 moved mimebundle to data attribute of output
                    data = data.data;
                }
                if (data['text/html'] == html_output) {
                    return [cell, data, j];
                }
            }
        }
    }
}

// Register the function which deals with the matplotlib target/channel.
// The kernel may be null if the page has been refreshed.
if (IPython.notebook.kernel != null) {
    IPython.notebook.kernel.comm_manager.register_target('matplotlib', mpl.mpl_figure_comm);
}

</script>
</div>

</div>

<div class="output_area"><div class="prompt"></div>

<div class="output_html rendered_html output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAoAAAAG4CAYAAADVDFZ+AAAgAElEQVR4Xuy9fZxcZXn/f91nZpOQsEHMxvIQHrI75z6zRFFEpRUbE1u0WrWotdq031J5UFtBRUAtKorBfita8qOttgpYFb9aq1ZrxaciqNBWsGolQPbcZzbBuATRDUU22TzNnPv3ujZn1smy2Tm755Nkd+cz/0B2zlwz874/59zvuc6TET5IgARIgARIgARIgAQ6ioDpqG/LL0sCJEACJEACJEACJCAUQIaABEiABEiABEiABDqMAAWwwwacX5cESIAESIAESIAEKIDMAAmQAAmQAAmQAAl0GAEKYIcNOL8uCZAACZAACZAACVAAmQESIAESIAESIAES6DACFMAOG3B+XRIgARIgARIgARKgADIDJEACJEACJEACJNBhBCiAHTbg/LokQAIkQAIkQAIkQAFkBkiABEiABEiABEigwwhQADtswPl1SYAESIAESIAESIACyAyQAAmQAAmQAAmQQIcRoAB22IDz65IACZAACZAACZAABZAZIAESIAESIAESIIEOI0AB7LAB59clARIgARIgARIgAQogM0ACJEACJEACJEACHUaAAthhA86vSwIkQAIkQAIkQAIUQGaABEiABEiABEiABDqMAAWwwwacX5cESIAESIAESIAEKIDMAAmQAAmQAAmQAAl0GAEKYIcNOL8uCZAACZAACZAACVAAmQESIAESIAESIAES6DACFMAOG3B+XRIgARIgARIgARKgADIDJEACJEACJEACJNBhBCiAHTbg/LokQAIkQAIkQAIkQAFkBkiABEiABEiABEigwwhQADtswPl1SYAESIAESIAESIACyAzMaQJRFK2M43jLnP4Sh/HDn3rqqU8IgsBv3rz5l4fxbflWJDBOYMWKFUd1dXUt3bJly8NzBYt+5oULF3YPDg7+fK58Zn5OEmhHgALYjhCfhxKw1m7x3l+WJMm/tBa21v6tMWZJHMfnh2G4zhjzRufcr0/15mEYvtgY8z7n3FOhH/IIFouiqNt7f4uIPF1EvuycW9f8ONbavxCRK0XEi0hZRBaKyE4R0fXYp2l6Wq1WG5ri4xtr7S+MMc+L4/ieNl+zZK3dZ4x52mTLWmt/aox5QxzHXz6CuGb01mEYvjMIgv44jv9oRgVm8CJrrY7LE0Wknr18bMy89+9P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">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="k">print</span> <span class="s">&quot;% 90 of converted test group users have encountered an impression less than &quot;</span><span class="p">,</span> \
<span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)]</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.90</span><span class="p">)</span>

<span class="k">print</span> <span class="s">&quot;% 80 of converted test group users have encountered an impression less than &quot;</span><span class="p">,</span> \
<span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)]</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.80</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>% 90 of converted test group users have encountered an impression less than  160.0
% 80 of converted test group users have encountered an impression less than  116.0
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 10. Plot histogram of impressions for converted control-group users</span>

<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">df</span><span class="p">[(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">)][</span><span class="s">&quot;tot_impr&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">values</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="s">&quot;auto&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s">&#39;Total Impressions&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s">&#39;Frequency&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s">&#39;Histogram of Total Impressions For Converted Control Group&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span> <span class="mi">600</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="mi">100</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>


<div class="output_subarea output_javascript ">
<script type="text/javascript">
/* Put everything inside the global mpl namespace */
window.mpl = {};

mpl.get_websocket_type = function() {
    if (typeof(WebSocket) !== 'undefined') {
        return WebSocket;
    } else if (typeof(MozWebSocket) !== 'undefined') {
        return MozWebSocket;
    } else {
        alert('Your browser does not have WebSocket support.' +
              'Please try Chrome, Safari or Firefox ≥ 6. ' +
              'Firefox 4 and 5 are also supported but you ' +
              'have to enable WebSockets in about:config.');
    };
}

mpl.figure = function(figure_id, websocket, ondownload, parent_element) {
    this.id = figure_id;

    this.ws = websocket;

    this.supports_binary = (this.ws.binaryType != undefined);

    if (!this.supports_binary) {
        var warnings = document.getElementById("mpl-warnings");
        if (warnings) {
            warnings.style.display = 'block';
            warnings.textContent = (
                "This browser does not support binary websocket messages. " +
                    "Performance may be slow.");
        }
    }

    this.imageObj = new Image();

    this.context = undefined;
    this.message = undefined;
    this.canvas = undefined;
    this.rubberband_canvas = undefined;
    this.rubberband_context = undefined;
    this.format_dropdown = undefined;

    this.image_mode = 'full';

    this.root = $('<div/>');
    this._root_extra_style(this.root)
    this.root.attr('style', 'display: inline-block');

    $(parent_element).append(this.root);

    this._init_header(this);
    this._init_canvas(this);
    this._init_toolbar(this);

    var fig = this;

    this.waiting = false;

    this.ws.onopen =  function () {
            fig.send_message("supports_binary", {value: fig.supports_binary});
            fig.send_message("send_image_mode", {});
            fig.send_message("refresh", {});
        }

    this.imageObj.onload = function() {
            if (fig.image_mode == 'full') {
                // Full images could contain transparency (where diff images
                // almost always do), so we need to clear the canvas so that
                // there is no ghosting.
                fig.context.clearRect(0, 0, fig.canvas.width, fig.canvas.height);
            }
            fig.context.drawImage(fig.imageObj, 0, 0);
        };

    this.imageObj.onunload = function() {
        this.ws.close();
    }

    this.ws.onmessage = this._make_on_message_function(this);

    this.ondownload = ondownload;
}

mpl.figure.prototype._init_header = function() {
    var titlebar = $(
        '<div class="ui-dialog-titlebar ui-widget-header ui-corner-all ' +
        'ui-helper-clearfix"/>');
    var titletext = $(
        '<div class="ui-dialog-title" style="width: 100%; ' +
        'text-align: center; padding: 3px;"/>');
    titlebar.append(titletext)
    this.root.append(titlebar);
    this.header = titletext[0];
}



mpl.figure.prototype._canvas_extra_style = function(canvas_div) {

}


mpl.figure.prototype._root_extra_style = function(canvas_div) {

}

mpl.figure.prototype._init_canvas = function() {
    var fig = this;

    var canvas_div = $('<div/>');

    canvas_div.attr('style', 'position: relative; clear: both; outline: 0');

    function canvas_keyboard_event(event) {
        return fig.key_event(event, event['data']);
    }

    canvas_div.keydown('key_press', canvas_keyboard_event);
    canvas_div.keyup('key_release', canvas_keyboard_event);
    this.canvas_div = canvas_div
    this._canvas_extra_style(canvas_div)
    this.root.append(canvas_div);

    var canvas = $('<canvas/>');
    canvas.addClass('mpl-canvas');
    canvas.attr('style', "left: 0; top: 0; z-index: 0; outline: 0")

    this.canvas = canvas[0];
    this.context = canvas[0].getContext("2d");

    var rubberband = $('<canvas/>');
    rubberband.attr('style', "position: absolute; left: 0; top: 0; z-index: 1;")

    var pass_mouse_events = true;

    canvas_div.resizable({
        start: function(event, ui) {
            pass_mouse_events = false;
        },
        resize: function(event, ui) {
            fig.request_resize(ui.size.width, ui.size.height);
        },
        stop: function(event, ui) {
            pass_mouse_events = true;
            fig.request_resize(ui.size.width, ui.size.height);
        },
    });

    function mouse_event_fn(event) {
        if (pass_mouse_events)
            return fig.mouse_event(event, event['data']);
    }

    rubberband.mousedown('button_press', mouse_event_fn);
    rubberband.mouseup('button_release', mouse_event_fn);
    // Throttle sequential mouse events to 1 every 20ms.
    rubberband.mousemove('motion_notify', mouse_event_fn);

    rubberband.mouseenter('figure_enter', mouse_event_fn);
    rubberband.mouseleave('figure_leave', mouse_event_fn);

    canvas_div.on("wheel", function (event) {
        event = event.originalEvent;
        event['data'] = 'scroll'
        if (event.deltaY < 0) {
            event.step = 1;
        } else {
            event.step = -1;
        }
        mouse_event_fn(event);
    });

    canvas_div.append(canvas);
    canvas_div.append(rubberband);

    this.rubberband = rubberband;
    this.rubberband_canvas = rubberband[0];
    this.rubberband_context = rubberband[0].getContext("2d");
    this.rubberband_context.strokeStyle = "#000000";

    this._resize_canvas = function(width, height) {
        // Keep the size of the canvas, canvas container, and rubber band
        // canvas in synch.
        canvas_div.css('width', width)
        canvas_div.css('height', height)

        canvas.attr('width', width);
        canvas.attr('height', height);

        rubberband.attr('width', width);
        rubberband.attr('height', height);
    }

    // Set the figure to an initial 600x600px, this will subsequently be updated
    // upon first draw.
    this._resize_canvas(600, 600);

    // Disable right mouse context menu.
    $(this.rubberband_canvas).bind("contextmenu",function(e){
        return false;
    });

    function set_focus () {
        canvas.focus();
        canvas_div.focus();
    }

    window.setTimeout(set_focus, 100);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items) {
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) {
            // put a spacer in here.
            continue;
        }
        var button = $('<button/>');
        button.addClass('ui-button ui-widget ui-state-default ui-corner-all ' +
                        'ui-button-icon-only');
        button.attr('role', 'button');
        button.attr('aria-disabled', 'false');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);

        var icon_img = $('<span/>');
        icon_img.addClass('ui-button-icon-primary ui-icon');
        icon_img.addClass(image);
        icon_img.addClass('ui-corner-all');

        var tooltip_span = $('<span/>');
        tooltip_span.addClass('ui-button-text');
        tooltip_span.html(tooltip);

        button.append(icon_img);
        button.append(tooltip_span);

        nav_element.append(button);
    }

    var fmt_picker_span = $('<span/>');

    var fmt_picker = $('<select/>');
    fmt_picker.addClass('mpl-toolbar-option ui-widget ui-widget-content');
    fmt_picker_span.append(fmt_picker);
    nav_element.append(fmt_picker_span);
    this.format_dropdown = fmt_picker[0];

    for (var ind in mpl.extensions) {
        var fmt = mpl.extensions[ind];
        var option = $(
            '<option/>', {selected: fmt === mpl.default_extension}).html(fmt);
        fmt_picker.append(option)
    }

    // Add hover states to the ui-buttons
    $( ".ui-button" ).hover(
        function() { $(this).addClass("ui-state-hover");},
        function() { $(this).removeClass("ui-state-hover");}
    );

    var status_bar = $('<span class="mpl-message"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];
}

mpl.figure.prototype.request_resize = function(x_pixels, y_pixels) {
    // Request matplotlib to resize the figure. Matplotlib will then trigger a resize in the client,
    // which will in turn request a refresh of the image.
    this.send_message('resize', {'width': x_pixels, 'height': y_pixels});
}

mpl.figure.prototype.send_message = function(type, properties) {
    properties['type'] = type;
    properties['figure_id'] = this.id;
    this.ws.send(JSON.stringify(properties));
}

mpl.figure.prototype.send_draw_message = function() {
    if (!this.waiting) {
        this.waiting = true;
        this.ws.send(JSON.stringify({type: "draw", figure_id: this.id}));
    }
}


mpl.figure.prototype.handle_save = function(fig, msg) {
    var format_dropdown = fig.format_dropdown;
    var format = format_dropdown.options[format_dropdown.selectedIndex].value;
    fig.ondownload(fig, format);
}


mpl.figure.prototype.handle_resize = function(fig, msg) {
    var size = msg['size'];
    if (size[0] != fig.canvas.width || size[1] != fig.canvas.height) {
        fig._resize_canvas(size[0], size[1]);
        fig.send_message("refresh", {});
    };
}

mpl.figure.prototype.handle_rubberband = function(fig, msg) {
    var x0 = msg['x0'];
    var y0 = fig.canvas.height - msg['y0'];
    var x1 = msg['x1'];
    var y1 = fig.canvas.height - msg['y1'];
    x0 = Math.floor(x0) + 0.5;
    y0 = Math.floor(y0) + 0.5;
    x1 = Math.floor(x1) + 0.5;
    y1 = Math.floor(y1) + 0.5;
    var min_x = Math.min(x0, x1);
    var min_y = Math.min(y0, y1);
    var width = Math.abs(x1 - x0);
    var height = Math.abs(y1 - y0);

    fig.rubberband_context.clearRect(
        0, 0, fig.canvas.width, fig.canvas.height);

    fig.rubberband_context.strokeRect(min_x, min_y, width, height);
}

mpl.figure.prototype.handle_figure_label = function(fig, msg) {
    // Updates the figure title.
    fig.header.textContent = msg['label'];
}

mpl.figure.prototype.handle_cursor = function(fig, msg) {
    var cursor = msg['cursor'];
    switch(cursor)
    {
    case 0:
        cursor = 'pointer';
        break;
    case 1:
        cursor = 'default';
        break;
    case 2:
        cursor = 'crosshair';
        break;
    case 3:
        cursor = 'move';
        break;
    }
    fig.rubberband_canvas.style.cursor = cursor;
}

mpl.figure.prototype.handle_message = function(fig, msg) {
    fig.message.textContent = msg['message'];
}

mpl.figure.prototype.handle_draw = function(fig, msg) {
    // Request the server to send over a new figure.
    fig.send_draw_message();
}

mpl.figure.prototype.handle_image_mode = function(fig, msg) {
    fig.image_mode = msg['mode'];
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Called whenever the canvas gets updated.
    this.send_message("ack", {});
}

// A function to construct a web socket function for onmessage handling.
// Called in the figure constructor.
mpl.figure.prototype._make_on_message_function = function(fig) {
    return function socket_on_message(evt) {
        if (evt.data instanceof Blob) {
            /* FIXME: We get "Resource interpreted as Image but
             * transferred with MIME type text/plain:" errors on
             * Chrome.  But how to set the MIME type?  It doesn't seem
             * to be part of the websocket stream */
            evt.data.type = "image/png";

            /* Free the memory for the previous frames */
            if (fig.imageObj.src) {
                (window.URL || window.webkitURL).revokeObjectURL(
                    fig.imageObj.src);
            }

            fig.imageObj.src = (window.URL || window.webkitURL).createObjectURL(
                evt.data);
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }
        else if (typeof evt.data === 'string' && evt.data.slice(0, 21) == "data:image/png;base64") {
            fig.imageObj.src = evt.data;
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }

        var msg = JSON.parse(evt.data);
        var msg_type = msg['type'];

        // Call the  "handle_{type}" callback, which takes
        // the figure and JSON message as its only arguments.
        try {
            var callback = fig["handle_" + msg_type];
        } catch (e) {
            console.log("No handler for the '" + msg_type + "' message type: ", msg);
            return;
        }

        if (callback) {
            try {
                // console.log("Handling '" + msg_type + "' message: ", msg);
                callback(fig, msg);
            } catch (e) {
                console.log("Exception inside the 'handler_" + msg_type + "' callback:", e, e.stack, msg);
            }
        }
    };
}

// from http://stackoverflow.com/questions/1114465/getting-mouse-location-in-canvas
mpl.findpos = function(e) {
    //this section is from http://www.quirksmode.org/js/events_properties.html
    var targ;
    if (!e)
        e = window.event;
    if (e.target)
        targ = e.target;
    else if (e.srcElement)
        targ = e.srcElement;
    if (targ.nodeType == 3) // defeat Safari bug
        targ = targ.parentNode;

    // jQuery normalizes the pageX and pageY
    // pageX,Y are the mouse positions relative to the document
    // offset() returns the position of the element relative to the document
    var x = e.pageX - $(targ).offset().left;
    var y = e.pageY - $(targ).offset().top;

    return {"x": x, "y": y};
};

/*
 * return a copy of an object with only non-object keys
 * we need this to avoid circular references
 * http://stackoverflow.com/a/24161582/3208463
 */
function simpleKeys (original) {
  return Object.keys(original).reduce(function (obj, key) {
    if (typeof original[key] !== 'object')
        obj[key] = original[key]
    return obj;
  }, {});
}

mpl.figure.prototype.mouse_event = function(event, name) {
    var canvas_pos = mpl.findpos(event)

    if (name === 'button_press')
    {
        this.canvas.focus();
        this.canvas_div.focus();
    }

    var x = canvas_pos.x;
    var y = canvas_pos.y;

    this.send_message(name, {x: x, y: y, button: event.button,
                             step: event.step,
                             guiEvent: simpleKeys(event)});

    /* This prevents the web browser from automatically changing to
     * the text insertion cursor when the button is pressed.  We want
     * to control all of the cursor setting manually through the
     * 'cursor' event from matplotlib */
    event.preventDefault();
    return false;
}

mpl.figure.prototype._key_event_extra = function(event, name) {
    // Handle any extra behaviour associated with a key event
}

mpl.figure.prototype.key_event = function(event, name) {

    // Prevent repeat events
    if (name == 'key_press')
    {
        if (event.which === this._key)
            return;
        else
            this._key = event.which;
    }
    if (name == 'key_release')
        this._key = null;

    var value = '';
    if (event.ctrlKey && event.which != 17)
        value += "ctrl+";
    if (event.altKey && event.which != 18)
        value += "alt+";
    if (event.shiftKey && event.which != 16)
        value += "shift+";

    value += 'k';
    value += event.which.toString();

    this._key_event_extra(event, name);

    this.send_message(name, {key: value,
                             guiEvent: simpleKeys(event)});
    return false;
}

mpl.figure.prototype.toolbar_button_onclick = function(name) {
    if (name == 'download') {
        this.handle_save(this, null);
    } else {
        this.send_message("toolbar_button", {name: name});
    }
};

mpl.figure.prototype.toolbar_button_onmouseover = function(tooltip) {
    this.message.textContent = tooltip;
};
mpl.toolbar_items = [["Home", "Reset original view", "fa fa-home icon-home", "home"], ["Back", "Back to  previous view", "fa fa-arrow-left icon-arrow-left", "back"], ["Forward", "Forward to next view", "fa fa-arrow-right icon-arrow-right", "forward"], ["", "", "", ""], ["Pan", "Pan axes with left mouse, zoom with right", "fa fa-arrows icon-move", "pan"], ["Zoom", "Zoom to rectangle", "fa fa-square-o icon-check-empty", "zoom"], ["", "", "", ""], ["Download", "Download plot", "fa fa-floppy-o icon-save", "download"]];

mpl.extensions = ["eps", "jpeg", "pdf", "png", "ps", "raw", "svg", "tif"];

mpl.default_extension = "png";var comm_websocket_adapter = function(comm) {
    // Create a "websocket"-like object which calls the given IPython comm
    // object with the appropriate methods. Currently this is a non binary
    // socket, so there is still some room for performance tuning.
    var ws = {};

    ws.close = function() {
        comm.close()
    };
    ws.send = function(m) {
        //console.log('sending', m);
        comm.send(m);
    };
    // Register the callback with on_msg.
    comm.on_msg(function(msg) {
        //console.log('receiving', msg['content']['data'], msg);
        // Pass the mpl event to the overriden (by mpl) onmessage function.
        ws.onmessage(msg['content']['data'])
    });
    return ws;
}

mpl.mpl_figure_comm = function(comm, msg) {
    // This is the function which gets called when the mpl process
    // starts-up an IPython Comm through the "matplotlib" channel.

    var id = msg.content.data.id;
    // Get hold of the div created by the display call when the Comm
    // socket was opened in Python.
    var element = $("#" + id);
    var ws_proxy = comm_websocket_adapter(comm)

    function ondownload(figure, format) {
        window.open(figure.imageObj.src);
    }

    var fig = new mpl.figure(id, ws_proxy,
                           ondownload,
                           element.get(0));

    // Call onopen now - mpl needs it, as it is assuming we've passed it a real
    // web socket which is closed, not our websocket->open comm proxy.
    ws_proxy.onopen();

    fig.parent_element = element.get(0);
    fig.cell_info = mpl.find_output_cell("<div id='" + id + "'></div>");
    if (!fig.cell_info) {
        console.error("Failed to find cell for figure", id, fig);
        return;
    }

    var output_index = fig.cell_info[2]
    var cell = fig.cell_info[0];

};

mpl.figure.prototype.handle_close = function(fig, msg) {
    fig.root.unbind('remove')

    // Update the output cell to use the data from the current canvas.
    fig.push_to_output();
    var dataURL = fig.canvas.toDataURL();
    // Re-enable the keyboard manager in IPython - without this line, in FF,
    // the notebook keyboard shortcuts fail.
    IPython.keyboard_manager.enable()
    $(fig.parent_element).html('<img src="' + dataURL + '">');
    fig.close_ws(fig, msg);
}

mpl.figure.prototype.close_ws = function(fig, msg){
    fig.send_message('closing', msg);
    // fig.ws.close()
}

mpl.figure.prototype.push_to_output = function(remove_interactive) {
    // Turn the data on the canvas into data in the output cell.
    var dataURL = this.canvas.toDataURL();
    this.cell_info[1]['text/html'] = '<img src="' + dataURL + '">';
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Tell IPython that the notebook contents must change.
    IPython.notebook.set_dirty(true);
    this.send_message("ack", {});
    var fig = this;
    // Wait a second, then push the new image to the DOM so
    // that it is saved nicely (might be nice to debounce this).
    setTimeout(function () { fig.push_to_output() }, 1000);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items){
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) { continue; };

        var button = $('<button class="btn btn-default" href="#" title="' + name + '"><i class="fa ' + image + ' fa-lg"></i></button>');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);
        nav_element.append(button);
    }

    // Add the status bar.
    var status_bar = $('<span class="mpl-message" style="text-align:right; float: right;"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];

    // Add the close button to the window.
    var buttongrp = $('<div class="btn-group inline pull-right"></div>');
    var button = $('<button class="btn btn-mini btn-primary" href="#" title="Stop Interaction"><i class="fa fa-power-off icon-remove icon-large"></i></button>');
    button.click(function (evt) { fig.handle_close(fig, {}); } );
    button.mouseover('Stop Interaction', toolbar_mouse_event);
    buttongrp.append(button);
    var titlebar = this.root.find($('.ui-dialog-titlebar'));
    titlebar.prepend(buttongrp);
}

mpl.figure.prototype._root_extra_style = function(el){
    var fig = this
    el.on("remove", function(){
	fig.close_ws(fig, {});
    });
}

mpl.figure.prototype._canvas_extra_style = function(el){
    // this is important to make the div 'focusable
    el.attr('tabindex', 0)
    // reach out to IPython and tell the keyboard manager to turn it's self
    // off when our div gets focus

    // location in version 3
    if (IPython.notebook.keyboard_manager) {
        IPython.notebook.keyboard_manager.register_events(el);
    }
    else {
        // location in version 2
        IPython.keyboard_manager.register_events(el);
    }

}

mpl.figure.prototype._key_event_extra = function(event, name) {
    var manager = IPython.notebook.keyboard_manager;
    if (!manager)
        manager = IPython.keyboard_manager;

    // Check for shift+enter
    if (event.shiftKey && event.which == 13) {
        this.canvas_div.blur();
        event.shiftKey = false;
        // Send a "J" for go to next cell
        event.which = 74;
        event.keyCode = 74;
        manager.command_mode();
        manager.handle_keydown(event);
    }
}

mpl.figure.prototype.handle_save = function(fig, msg) {
    fig.ondownload(fig, null);
}


mpl.find_output_cell = function(html_output) {
    // Return the cell and output element which can be found *uniquely* in the notebook.
    // Note - this is a bit hacky, but it is done because the "notebook_saving.Notebook"
    // IPython event is triggered only after the cells have been serialised, which for
    // our purposes (turning an active figure into a static one), is too late.
    var cells = IPython.notebook.get_cells();
    var ncells = cells.length;
    for (var i=0; i<ncells; i++) {
        var cell = cells[i];
        if (cell.cell_type === 'code'){
            for (var j=0; j<cell.output_area.outputs.length; j++) {
                var data = cell.output_area.outputs[j];
                if (data.data) {
                    // IPython >= 3 moved mimebundle to data attribute of output
                    data = data.data;
                }
                if (data['text/html'] == html_output) {
                    return [cell, data, j];
                }
            }
        }
    }
}

// Register the function which deals with the matplotlib target/channel.
// The kernel may be null if the page has been refreshed.
if (IPython.notebook.kernel != null) {
    IPython.notebook.kernel.comm_manager.register_target('matplotlib', mpl.mpl_figure_comm);
}

</script>
</div>

</div>

<div class="output_area"><div class="prompt"></div>

<div class="output_html rendered_html output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAoAAAAG4CAYAAADVDFZ+AAAgAElEQVR4XuydeZxcVZn3n3OrOgkJHbZESYhI0lWnuhPABZUZR1l0cBt1GGd0HNQXBdxGUFYXHFEEfcdl8B0XZgYQ1xnHbVxxXBEFnUHHjS19z60kDIYgGBToJCTpqnvez5PcCk3b3XW6zi9JVepX/yipc5++93uee8+3nnPuvUb4IQESIAESIAESIAES6CsCpq+OlgdLAiRAAiRAAiRAAiQgFEAmAQmQAAmQAAmQAAn0GQEKYJ91OA+XBEiABEiABEiABCiAzAESIAESIAESIAES6DMCFMA+63AeLgmQAAmQAAmQAAlQAJkDJEACJEACJEACJNBnBCiAfdbhPFwSIAESIAESIAESoAAyB0iABEiABEiABEigzwhQAPusw3m4JEACJEACJEACJEABZA6QAAmQAAmQAAmQQJ8RoAD2WYfzcEmABEiABEiABEiAAsgcIAESIAESIAESIIE+I0AB7LMO5+GSAAmQAAmQAAmQAAWQOUACJEACJEACJEACfUaAAthnHc7DJQESIAESIAESIAEKIHOABEiABEiABEiABPqMAAWwzzqch0sCJEACJEACJEACFEDmAAmQAAmQAAmQAAn0GQEKYJ91OA+XBEiABEiABEiABCiAzAESIAESIAESIAES6DMCFMA+63AeLgmQAAmQAAmQAAlQAJkDJEACJEACJEACJNBnBCiAfdbhPFwSIAESIAESIAESoAAyB0iABEiABEiABEigzwhQAPusw3m4JEACJEACJEACJEABZA6QAAmQAAmQAAmQQJ8RoAD2WYfzcEmABEiABEiABEiAAsgc6FoCtVpteZqm67p2B7tsx4444ogDkyTxa9euvb/Ldo270ycEli1btt/AwMDCdevW3d1rh8zzp9d6jPsbS4ACGEuQ2+8iYK1d570/L8uy/5iIxVr7IWPMgjRNT6tWq6cYY17vnPujmdBVq9XnGmPe5Zx7zL6CuFarDXrvrxGRx4vIV51zp7SOzVr7FhG5UES8iJRFZK6IbBYRPUd9nucr6/X6+hlYGGvtb40xT0vT9KY2zErW2nFjzGOnamut/bUx5nVpmn6119hXq9W/S5JkJE3Tl+ypfbfWar8cLCKN4m/u6DPv/XuyLHsXYj9qtdoLvfdnishRItIUkf/x3r8j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">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="k">print</span> <span class="s">&quot;% 90 of converted control group users have encountered an impression less than &quot;</span><span class="p">,</span> \
<span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">)]</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.90</span><span class="p">)</span>

<span class="k">print</span> <span class="s">&quot;% 80 of converted control group users have encountered an impression less than &quot;</span><span class="p">,</span> \
<span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">)]</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.80</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>% 90 of converted control group users have encountered an impression less than  52.0
% 80 of converted control group users have encountered an impression less than  31.0
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 11. Bar plot of impressions vs. day of week</span>

<span class="n">ggplot</span><span class="p">(</span><span class="n">aes</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s">&#39;mode_impr_day&#39;</span><span class="p">),</span> <span class="n">data</span><span class="o">=</span><span class="n">df</span><span class="p">)</span> <span class="o">+</span> \
     <span class="n">xlab</span><span class="p">(</span><span class="s">&quot;Days&quot;</span><span class="p">)</span> <span class="o">+</span> <span class="n">ylab</span><span class="p">(</span><span class="s">&quot;Impressions&quot;</span><span class="p">)</span> <span class="o">+</span> <span class="n">ggtitle</span><span class="p">(</span><span class="s">&quot;Impressions Vs. Day of Week&quot;</span><span class="p">)</span> <span class="o">+</span> <span class="n">geom_bar</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>


<div class="output_subarea output_javascript ">
<script type="text/javascript">
/* Put everything inside the global mpl namespace */
window.mpl = {};

mpl.get_websocket_type = function() {
    if (typeof(WebSocket) !== 'undefined') {
        return WebSocket;
    } else if (typeof(MozWebSocket) !== 'undefined') {
        return MozWebSocket;
    } else {
        alert('Your browser does not have WebSocket support.' +
              'Please try Chrome, Safari or Firefox ≥ 6. ' +
              'Firefox 4 and 5 are also supported but you ' +
              'have to enable WebSockets in about:config.');
    };
}

mpl.figure = function(figure_id, websocket, ondownload, parent_element) {
    this.id = figure_id;

    this.ws = websocket;

    this.supports_binary = (this.ws.binaryType != undefined);

    if (!this.supports_binary) {
        var warnings = document.getElementById("mpl-warnings");
        if (warnings) {
            warnings.style.display = 'block';
            warnings.textContent = (
                "This browser does not support binary websocket messages. " +
                    "Performance may be slow.");
        }
    }

    this.imageObj = new Image();

    this.context = undefined;
    this.message = undefined;
    this.canvas = undefined;
    this.rubberband_canvas = undefined;
    this.rubberband_context = undefined;
    this.format_dropdown = undefined;

    this.image_mode = 'full';

    this.root = $('<div/>');
    this._root_extra_style(this.root)
    this.root.attr('style', 'display: inline-block');

    $(parent_element).append(this.root);

    this._init_header(this);
    this._init_canvas(this);
    this._init_toolbar(this);

    var fig = this;

    this.waiting = false;

    this.ws.onopen =  function () {
            fig.send_message("supports_binary", {value: fig.supports_binary});
            fig.send_message("send_image_mode", {});
            fig.send_message("refresh", {});
        }

    this.imageObj.onload = function() {
            if (fig.image_mode == 'full') {
                // Full images could contain transparency (where diff images
                // almost always do), so we need to clear the canvas so that
                // there is no ghosting.
                fig.context.clearRect(0, 0, fig.canvas.width, fig.canvas.height);
            }
            fig.context.drawImage(fig.imageObj, 0, 0);
        };

    this.imageObj.onunload = function() {
        this.ws.close();
    }

    this.ws.onmessage = this._make_on_message_function(this);

    this.ondownload = ondownload;
}

mpl.figure.prototype._init_header = function() {
    var titlebar = $(
        '<div class="ui-dialog-titlebar ui-widget-header ui-corner-all ' +
        'ui-helper-clearfix"/>');
    var titletext = $(
        '<div class="ui-dialog-title" style="width: 100%; ' +
        'text-align: center; padding: 3px;"/>');
    titlebar.append(titletext)
    this.root.append(titlebar);
    this.header = titletext[0];
}



mpl.figure.prototype._canvas_extra_style = function(canvas_div) {

}


mpl.figure.prototype._root_extra_style = function(canvas_div) {

}

mpl.figure.prototype._init_canvas = function() {
    var fig = this;

    var canvas_div = $('<div/>');

    canvas_div.attr('style', 'position: relative; clear: both; outline: 0');

    function canvas_keyboard_event(event) {
        return fig.key_event(event, event['data']);
    }

    canvas_div.keydown('key_press', canvas_keyboard_event);
    canvas_div.keyup('key_release', canvas_keyboard_event);
    this.canvas_div = canvas_div
    this._canvas_extra_style(canvas_div)
    this.root.append(canvas_div);

    var canvas = $('<canvas/>');
    canvas.addClass('mpl-canvas');
    canvas.attr('style', "left: 0; top: 0; z-index: 0; outline: 0")

    this.canvas = canvas[0];
    this.context = canvas[0].getContext("2d");

    var rubberband = $('<canvas/>');
    rubberband.attr('style', "position: absolute; left: 0; top: 0; z-index: 1;")

    var pass_mouse_events = true;

    canvas_div.resizable({
        start: function(event, ui) {
            pass_mouse_events = false;
        },
        resize: function(event, ui) {
            fig.request_resize(ui.size.width, ui.size.height);
        },
        stop: function(event, ui) {
            pass_mouse_events = true;
            fig.request_resize(ui.size.width, ui.size.height);
        },
    });

    function mouse_event_fn(event) {
        if (pass_mouse_events)
            return fig.mouse_event(event, event['data']);
    }

    rubberband.mousedown('button_press', mouse_event_fn);
    rubberband.mouseup('button_release', mouse_event_fn);
    // Throttle sequential mouse events to 1 every 20ms.
    rubberband.mousemove('motion_notify', mouse_event_fn);

    rubberband.mouseenter('figure_enter', mouse_event_fn);
    rubberband.mouseleave('figure_leave', mouse_event_fn);

    canvas_div.on("wheel", function (event) {
        event = event.originalEvent;
        event['data'] = 'scroll'
        if (event.deltaY < 0) {
            event.step = 1;
        } else {
            event.step = -1;
        }
        mouse_event_fn(event);
    });

    canvas_div.append(canvas);
    canvas_div.append(rubberband);

    this.rubberband = rubberband;
    this.rubberband_canvas = rubberband[0];
    this.rubberband_context = rubberband[0].getContext("2d");
    this.rubberband_context.strokeStyle = "#000000";

    this._resize_canvas = function(width, height) {
        // Keep the size of the canvas, canvas container, and rubber band
        // canvas in synch.
        canvas_div.css('width', width)
        canvas_div.css('height', height)

        canvas.attr('width', width);
        canvas.attr('height', height);

        rubberband.attr('width', width);
        rubberband.attr('height', height);
    }

    // Set the figure to an initial 600x600px, this will subsequently be updated
    // upon first draw.
    this._resize_canvas(600, 600);

    // Disable right mouse context menu.
    $(this.rubberband_canvas).bind("contextmenu",function(e){
        return false;
    });

    function set_focus () {
        canvas.focus();
        canvas_div.focus();
    }

    window.setTimeout(set_focus, 100);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items) {
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) {
            // put a spacer in here.
            continue;
        }
        var button = $('<button/>');
        button.addClass('ui-button ui-widget ui-state-default ui-corner-all ' +
                        'ui-button-icon-only');
        button.attr('role', 'button');
        button.attr('aria-disabled', 'false');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);

        var icon_img = $('<span/>');
        icon_img.addClass('ui-button-icon-primary ui-icon');
        icon_img.addClass(image);
        icon_img.addClass('ui-corner-all');

        var tooltip_span = $('<span/>');
        tooltip_span.addClass('ui-button-text');
        tooltip_span.html(tooltip);

        button.append(icon_img);
        button.append(tooltip_span);

        nav_element.append(button);
    }

    var fmt_picker_span = $('<span/>');

    var fmt_picker = $('<select/>');
    fmt_picker.addClass('mpl-toolbar-option ui-widget ui-widget-content');
    fmt_picker_span.append(fmt_picker);
    nav_element.append(fmt_picker_span);
    this.format_dropdown = fmt_picker[0];

    for (var ind in mpl.extensions) {
        var fmt = mpl.extensions[ind];
        var option = $(
            '<option/>', {selected: fmt === mpl.default_extension}).html(fmt);
        fmt_picker.append(option)
    }

    // Add hover states to the ui-buttons
    $( ".ui-button" ).hover(
        function() { $(this).addClass("ui-state-hover");},
        function() { $(this).removeClass("ui-state-hover");}
    );

    var status_bar = $('<span class="mpl-message"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];
}

mpl.figure.prototype.request_resize = function(x_pixels, y_pixels) {
    // Request matplotlib to resize the figure. Matplotlib will then trigger a resize in the client,
    // which will in turn request a refresh of the image.
    this.send_message('resize', {'width': x_pixels, 'height': y_pixels});
}

mpl.figure.prototype.send_message = function(type, properties) {
    properties['type'] = type;
    properties['figure_id'] = this.id;
    this.ws.send(JSON.stringify(properties));
}

mpl.figure.prototype.send_draw_message = function() {
    if (!this.waiting) {
        this.waiting = true;
        this.ws.send(JSON.stringify({type: "draw", figure_id: this.id}));
    }
}


mpl.figure.prototype.handle_save = function(fig, msg) {
    var format_dropdown = fig.format_dropdown;
    var format = format_dropdown.options[format_dropdown.selectedIndex].value;
    fig.ondownload(fig, format);
}


mpl.figure.prototype.handle_resize = function(fig, msg) {
    var size = msg['size'];
    if (size[0] != fig.canvas.width || size[1] != fig.canvas.height) {
        fig._resize_canvas(size[0], size[1]);
        fig.send_message("refresh", {});
    };
}

mpl.figure.prototype.handle_rubberband = function(fig, msg) {
    var x0 = msg['x0'];
    var y0 = fig.canvas.height - msg['y0'];
    var x1 = msg['x1'];
    var y1 = fig.canvas.height - msg['y1'];
    x0 = Math.floor(x0) + 0.5;
    y0 = Math.floor(y0) + 0.5;
    x1 = Math.floor(x1) + 0.5;
    y1 = Math.floor(y1) + 0.5;
    var min_x = Math.min(x0, x1);
    var min_y = Math.min(y0, y1);
    var width = Math.abs(x1 - x0);
    var height = Math.abs(y1 - y0);

    fig.rubberband_context.clearRect(
        0, 0, fig.canvas.width, fig.canvas.height);

    fig.rubberband_context.strokeRect(min_x, min_y, width, height);
}

mpl.figure.prototype.handle_figure_label = function(fig, msg) {
    // Updates the figure title.
    fig.header.textContent = msg['label'];
}

mpl.figure.prototype.handle_cursor = function(fig, msg) {
    var cursor = msg['cursor'];
    switch(cursor)
    {
    case 0:
        cursor = 'pointer';
        break;
    case 1:
        cursor = 'default';
        break;
    case 2:
        cursor = 'crosshair';
        break;
    case 3:
        cursor = 'move';
        break;
    }
    fig.rubberband_canvas.style.cursor = cursor;
}

mpl.figure.prototype.handle_message = function(fig, msg) {
    fig.message.textContent = msg['message'];
}

mpl.figure.prototype.handle_draw = function(fig, msg) {
    // Request the server to send over a new figure.
    fig.send_draw_message();
}

mpl.figure.prototype.handle_image_mode = function(fig, msg) {
    fig.image_mode = msg['mode'];
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Called whenever the canvas gets updated.
    this.send_message("ack", {});
}

// A function to construct a web socket function for onmessage handling.
// Called in the figure constructor.
mpl.figure.prototype._make_on_message_function = function(fig) {
    return function socket_on_message(evt) {
        if (evt.data instanceof Blob) {
            /* FIXME: We get "Resource interpreted as Image but
             * transferred with MIME type text/plain:" errors on
             * Chrome.  But how to set the MIME type?  It doesn't seem
             * to be part of the websocket stream */
            evt.data.type = "image/png";

            /* Free the memory for the previous frames */
            if (fig.imageObj.src) {
                (window.URL || window.webkitURL).revokeObjectURL(
                    fig.imageObj.src);
            }

            fig.imageObj.src = (window.URL || window.webkitURL).createObjectURL(
                evt.data);
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }
        else if (typeof evt.data === 'string' && evt.data.slice(0, 21) == "data:image/png;base64") {
            fig.imageObj.src = evt.data;
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }

        var msg = JSON.parse(evt.data);
        var msg_type = msg['type'];

        // Call the  "handle_{type}" callback, which takes
        // the figure and JSON message as its only arguments.
        try {
            var callback = fig["handle_" + msg_type];
        } catch (e) {
            console.log("No handler for the '" + msg_type + "' message type: ", msg);
            return;
        }

        if (callback) {
            try {
                // console.log("Handling '" + msg_type + "' message: ", msg);
                callback(fig, msg);
            } catch (e) {
                console.log("Exception inside the 'handler_" + msg_type + "' callback:", e, e.stack, msg);
            }
        }
    };
}

// from http://stackoverflow.com/questions/1114465/getting-mouse-location-in-canvas
mpl.findpos = function(e) {
    //this section is from http://www.quirksmode.org/js/events_properties.html
    var targ;
    if (!e)
        e = window.event;
    if (e.target)
        targ = e.target;
    else if (e.srcElement)
        targ = e.srcElement;
    if (targ.nodeType == 3) // defeat Safari bug
        targ = targ.parentNode;

    // jQuery normalizes the pageX and pageY
    // pageX,Y are the mouse positions relative to the document
    // offset() returns the position of the element relative to the document
    var x = e.pageX - $(targ).offset().left;
    var y = e.pageY - $(targ).offset().top;

    return {"x": x, "y": y};
};

/*
 * return a copy of an object with only non-object keys
 * we need this to avoid circular references
 * http://stackoverflow.com/a/24161582/3208463
 */
function simpleKeys (original) {
  return Object.keys(original).reduce(function (obj, key) {
    if (typeof original[key] !== 'object')
        obj[key] = original[key]
    return obj;
  }, {});
}

mpl.figure.prototype.mouse_event = function(event, name) {
    var canvas_pos = mpl.findpos(event)

    if (name === 'button_press')
    {
        this.canvas.focus();
        this.canvas_div.focus();
    }

    var x = canvas_pos.x;
    var y = canvas_pos.y;

    this.send_message(name, {x: x, y: y, button: event.button,
                             step: event.step,
                             guiEvent: simpleKeys(event)});

    /* This prevents the web browser from automatically changing to
     * the text insertion cursor when the button is pressed.  We want
     * to control all of the cursor setting manually through the
     * 'cursor' event from matplotlib */
    event.preventDefault();
    return false;
}

mpl.figure.prototype._key_event_extra = function(event, name) {
    // Handle any extra behaviour associated with a key event
}

mpl.figure.prototype.key_event = function(event, name) {

    // Prevent repeat events
    if (name == 'key_press')
    {
        if (event.which === this._key)
            return;
        else
            this._key = event.which;
    }
    if (name == 'key_release')
        this._key = null;

    var value = '';
    if (event.ctrlKey && event.which != 17)
        value += "ctrl+";
    if (event.altKey && event.which != 18)
        value += "alt+";
    if (event.shiftKey && event.which != 16)
        value += "shift+";

    value += 'k';
    value += event.which.toString();

    this._key_event_extra(event, name);

    this.send_message(name, {key: value,
                             guiEvent: simpleKeys(event)});
    return false;
}

mpl.figure.prototype.toolbar_button_onclick = function(name) {
    if (name == 'download') {
        this.handle_save(this, null);
    } else {
        this.send_message("toolbar_button", {name: name});
    }
};

mpl.figure.prototype.toolbar_button_onmouseover = function(tooltip) {
    this.message.textContent = tooltip;
};
mpl.toolbar_items = [["Home", "Reset original view", "fa fa-home icon-home", "home"], ["Back", "Back to  previous view", "fa fa-arrow-left icon-arrow-left", "back"], ["Forward", "Forward to next view", "fa fa-arrow-right icon-arrow-right", "forward"], ["", "", "", ""], ["Pan", "Pan axes with left mouse, zoom with right", "fa fa-arrows icon-move", "pan"], ["Zoom", "Zoom to rectangle", "fa fa-square-o icon-check-empty", "zoom"], ["", "", "", ""], ["Download", "Download plot", "fa fa-floppy-o icon-save", "download"]];

mpl.extensions = ["eps", "jpeg", "pdf", "png", "ps", "raw", "svg", "tif"];

mpl.default_extension = "png";var comm_websocket_adapter = function(comm) {
    // Create a "websocket"-like object which calls the given IPython comm
    // object with the appropriate methods. Currently this is a non binary
    // socket, so there is still some room for performance tuning.
    var ws = {};

    ws.close = function() {
        comm.close()
    };
    ws.send = function(m) {
        //console.log('sending', m);
        comm.send(m);
    };
    // Register the callback with on_msg.
    comm.on_msg(function(msg) {
        //console.log('receiving', msg['content']['data'], msg);
        // Pass the mpl event to the overriden (by mpl) onmessage function.
        ws.onmessage(msg['content']['data'])
    });
    return ws;
}

mpl.mpl_figure_comm = function(comm, msg) {
    // This is the function which gets called when the mpl process
    // starts-up an IPython Comm through the "matplotlib" channel.

    var id = msg.content.data.id;
    // Get hold of the div created by the display call when the Comm
    // socket was opened in Python.
    var element = $("#" + id);
    var ws_proxy = comm_websocket_adapter(comm)

    function ondownload(figure, format) {
        window.open(figure.imageObj.src);
    }

    var fig = new mpl.figure(id, ws_proxy,
                           ondownload,
                           element.get(0));

    // Call onopen now - mpl needs it, as it is assuming we've passed it a real
    // web socket which is closed, not our websocket->open comm proxy.
    ws_proxy.onopen();

    fig.parent_element = element.get(0);
    fig.cell_info = mpl.find_output_cell("<div id='" + id + "'></div>");
    if (!fig.cell_info) {
        console.error("Failed to find cell for figure", id, fig);
        return;
    }

    var output_index = fig.cell_info[2]
    var cell = fig.cell_info[0];

};

mpl.figure.prototype.handle_close = function(fig, msg) {
    fig.root.unbind('remove')

    // Update the output cell to use the data from the current canvas.
    fig.push_to_output();
    var dataURL = fig.canvas.toDataURL();
    // Re-enable the keyboard manager in IPython - without this line, in FF,
    // the notebook keyboard shortcuts fail.
    IPython.keyboard_manager.enable()
    $(fig.parent_element).html('<img src="' + dataURL + '">');
    fig.close_ws(fig, msg);
}

mpl.figure.prototype.close_ws = function(fig, msg){
    fig.send_message('closing', msg);
    // fig.ws.close()
}

mpl.figure.prototype.push_to_output = function(remove_interactive) {
    // Turn the data on the canvas into data in the output cell.
    var dataURL = this.canvas.toDataURL();
    this.cell_info[1]['text/html'] = '<img src="' + dataURL + '">';
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Tell IPython that the notebook contents must change.
    IPython.notebook.set_dirty(true);
    this.send_message("ack", {});
    var fig = this;
    // Wait a second, then push the new image to the DOM so
    // that it is saved nicely (might be nice to debounce this).
    setTimeout(function () { fig.push_to_output() }, 1000);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items){
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) { continue; };

        var button = $('<button class="btn btn-default" href="#" title="' + name + '"><i class="fa ' + image + ' fa-lg"></i></button>');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);
        nav_element.append(button);
    }

    // Add the status bar.
    var status_bar = $('<span class="mpl-message" style="text-align:right; float: right;"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];

    // Add the close button to the window.
    var buttongrp = $('<div class="btn-group inline pull-right"></div>');
    var button = $('<button class="btn btn-mini btn-primary" href="#" title="Stop Interaction"><i class="fa fa-power-off icon-remove icon-large"></i></button>');
    button.click(function (evt) { fig.handle_close(fig, {}); } );
    button.mouseover('Stop Interaction', toolbar_mouse_event);
    buttongrp.append(button);
    var titlebar = this.root.find($('.ui-dialog-titlebar'));
    titlebar.prepend(buttongrp);
}

mpl.figure.prototype._root_extra_style = function(el){
    var fig = this
    el.on("remove", function(){
	fig.close_ws(fig, {});
    });
}

mpl.figure.prototype._canvas_extra_style = function(el){
    // this is important to make the div 'focusable
    el.attr('tabindex', 0)
    // reach out to IPython and tell the keyboard manager to turn it's self
    // off when our div gets focus

    // location in version 3
    if (IPython.notebook.keyboard_manager) {
        IPython.notebook.keyboard_manager.register_events(el);
    }
    else {
        // location in version 2
        IPython.keyboard_manager.register_events(el);
    }

}

mpl.figure.prototype._key_event_extra = function(event, name) {
    var manager = IPython.notebook.keyboard_manager;
    if (!manager)
        manager = IPython.keyboard_manager;

    // Check for shift+enter
    if (event.shiftKey && event.which == 13) {
        this.canvas_div.blur();
        event.shiftKey = false;
        // Send a "J" for go to next cell
        event.which = 74;
        event.keyCode = 74;
        manager.command_mode();
        manager.handle_keydown(event);
    }
}

mpl.figure.prototype.handle_save = function(fig, msg) {
    fig.ondownload(fig, null);
}


mpl.find_output_cell = function(html_output) {
    // Return the cell and output element which can be found *uniquely* in the notebook.
    // Note - this is a bit hacky, but it is done because the "notebook_saving.Notebook"
    // IPython event is triggered only after the cells have been serialised, which for
    // our purposes (turning an active figure into a static one), is too late.
    var cells = IPython.notebook.get_cells();
    var ncells = cells.length;
    for (var i=0; i<ncells; i++) {
        var cell = cells[i];
        if (cell.cell_type === 'code'){
            for (var j=0; j<cell.output_area.outputs.length; j++) {
                var data = cell.output_area.outputs[j];
                if (data.data) {
                    // IPython >= 3 moved mimebundle to data attribute of output
                    data = data.data;
                }
                if (data['text/html'] == html_output) {
                    return [cell, data, j];
                }
            }
        }
    }
}

// Register the function which deals with the matplotlib target/channel.
// The kernel may be null if the page has been refreshed.
if (IPython.notebook.kernel != null) {
    IPython.notebook.kernel.comm_manager.register_target('matplotlib', mpl.mpl_figure_comm);
}

</script>
</div>

</div>

<div class="output_area"><div class="prompt"></div>

<div class="output_html rendered_html output_subarea ">
<img src="data:image/png;base64,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">
</div>

</div>

<div class="output_area"><div class="prompt output_prompt">Out[15]:</div>


<div class="output_text output_subarea output_execute_result">
<pre>&lt;ggplot: (29800996)&gt;</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>By looking at this plot we can say that total number of impressions is almost consistent over day. 
Each day almost same amount of ad (around 8000) were shown to people.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># 12. Bar plot of impressions vs. hour of day</span>

<span class="n">ggplot</span><span class="p">(</span><span class="n">aes</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s">&#39;mode_impr_hour&#39;</span><span class="p">),</span> <span class="n">data</span><span class="o">=</span><span class="n">df</span><span class="p">[(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;mode_impr_hour&quot;</span><span class="p">]</span><span class="o">&gt;=</span><span class="mi">8</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;mode_impr_hour&quot;</span><span class="p">]</span><span class="o">&lt;=</span><span class="mi">23</span><span class="p">)])</span> <span class="o">+</span> \
     <span class="n">xlab</span><span class="p">(</span><span class="s">&quot;Hours&quot;</span><span class="p">)</span> <span class="o">+</span> <span class="n">ylab</span><span class="p">(</span><span class="s">&quot;Impressions&quot;</span><span class="p">)</span> <span class="o">+</span> <span class="n">ggtitle</span><span class="p">(</span><span class="s">&quot;Impressions Vs. Hour&quot;</span><span class="p">)</span> <span class="o">+</span> <span class="n">geom_bar</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>


<div class="output_subarea output_javascript ">
<script type="text/javascript">
/* Put everything inside the global mpl namespace */
window.mpl = {};

mpl.get_websocket_type = function() {
    if (typeof(WebSocket) !== 'undefined') {
        return WebSocket;
    } else if (typeof(MozWebSocket) !== 'undefined') {
        return MozWebSocket;
    } else {
        alert('Your browser does not have WebSocket support.' +
              'Please try Chrome, Safari or Firefox ≥ 6. ' +
              'Firefox 4 and 5 are also supported but you ' +
              'have to enable WebSockets in about:config.');
    };
}

mpl.figure = function(figure_id, websocket, ondownload, parent_element) {
    this.id = figure_id;

    this.ws = websocket;

    this.supports_binary = (this.ws.binaryType != undefined);

    if (!this.supports_binary) {
        var warnings = document.getElementById("mpl-warnings");
        if (warnings) {
            warnings.style.display = 'block';
            warnings.textContent = (
                "This browser does not support binary websocket messages. " +
                    "Performance may be slow.");
        }
    }

    this.imageObj = new Image();

    this.context = undefined;
    this.message = undefined;
    this.canvas = undefined;
    this.rubberband_canvas = undefined;
    this.rubberband_context = undefined;
    this.format_dropdown = undefined;

    this.image_mode = 'full';

    this.root = $('<div/>');
    this._root_extra_style(this.root)
    this.root.attr('style', 'display: inline-block');

    $(parent_element).append(this.root);

    this._init_header(this);
    this._init_canvas(this);
    this._init_toolbar(this);

    var fig = this;

    this.waiting = false;

    this.ws.onopen =  function () {
            fig.send_message("supports_binary", {value: fig.supports_binary});
            fig.send_message("send_image_mode", {});
            fig.send_message("refresh", {});
        }

    this.imageObj.onload = function() {
            if (fig.image_mode == 'full') {
                // Full images could contain transparency (where diff images
                // almost always do), so we need to clear the canvas so that
                // there is no ghosting.
                fig.context.clearRect(0, 0, fig.canvas.width, fig.canvas.height);
            }
            fig.context.drawImage(fig.imageObj, 0, 0);
        };

    this.imageObj.onunload = function() {
        this.ws.close();
    }

    this.ws.onmessage = this._make_on_message_function(this);

    this.ondownload = ondownload;
}

mpl.figure.prototype._init_header = function() {
    var titlebar = $(
        '<div class="ui-dialog-titlebar ui-widget-header ui-corner-all ' +
        'ui-helper-clearfix"/>');
    var titletext = $(
        '<div class="ui-dialog-title" style="width: 100%; ' +
        'text-align: center; padding: 3px;"/>');
    titlebar.append(titletext)
    this.root.append(titlebar);
    this.header = titletext[0];
}



mpl.figure.prototype._canvas_extra_style = function(canvas_div) {

}


mpl.figure.prototype._root_extra_style = function(canvas_div) {

}

mpl.figure.prototype._init_canvas = function() {
    var fig = this;

    var canvas_div = $('<div/>');

    canvas_div.attr('style', 'position: relative; clear: both; outline: 0');

    function canvas_keyboard_event(event) {
        return fig.key_event(event, event['data']);
    }

    canvas_div.keydown('key_press', canvas_keyboard_event);
    canvas_div.keyup('key_release', canvas_keyboard_event);
    this.canvas_div = canvas_div
    this._canvas_extra_style(canvas_div)
    this.root.append(canvas_div);

    var canvas = $('<canvas/>');
    canvas.addClass('mpl-canvas');
    canvas.attr('style', "left: 0; top: 0; z-index: 0; outline: 0")

    this.canvas = canvas[0];
    this.context = canvas[0].getContext("2d");

    var rubberband = $('<canvas/>');
    rubberband.attr('style', "position: absolute; left: 0; top: 0; z-index: 1;")

    var pass_mouse_events = true;

    canvas_div.resizable({
        start: function(event, ui) {
            pass_mouse_events = false;
        },
        resize: function(event, ui) {
            fig.request_resize(ui.size.width, ui.size.height);
        },
        stop: function(event, ui) {
            pass_mouse_events = true;
            fig.request_resize(ui.size.width, ui.size.height);
        },
    });

    function mouse_event_fn(event) {
        if (pass_mouse_events)
            return fig.mouse_event(event, event['data']);
    }

    rubberband.mousedown('button_press', mouse_event_fn);
    rubberband.mouseup('button_release', mouse_event_fn);
    // Throttle sequential mouse events to 1 every 20ms.
    rubberband.mousemove('motion_notify', mouse_event_fn);

    rubberband.mouseenter('figure_enter', mouse_event_fn);
    rubberband.mouseleave('figure_leave', mouse_event_fn);

    canvas_div.on("wheel", function (event) {
        event = event.originalEvent;
        event['data'] = 'scroll'
        if (event.deltaY < 0) {
            event.step = 1;
        } else {
            event.step = -1;
        }
        mouse_event_fn(event);
    });

    canvas_div.append(canvas);
    canvas_div.append(rubberband);

    this.rubberband = rubberband;
    this.rubberband_canvas = rubberband[0];
    this.rubberband_context = rubberband[0].getContext("2d");
    this.rubberband_context.strokeStyle = "#000000";

    this._resize_canvas = function(width, height) {
        // Keep the size of the canvas, canvas container, and rubber band
        // canvas in synch.
        canvas_div.css('width', width)
        canvas_div.css('height', height)

        canvas.attr('width', width);
        canvas.attr('height', height);

        rubberband.attr('width', width);
        rubberband.attr('height', height);
    }

    // Set the figure to an initial 600x600px, this will subsequently be updated
    // upon first draw.
    this._resize_canvas(600, 600);

    // Disable right mouse context menu.
    $(this.rubberband_canvas).bind("contextmenu",function(e){
        return false;
    });

    function set_focus () {
        canvas.focus();
        canvas_div.focus();
    }

    window.setTimeout(set_focus, 100);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items) {
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) {
            // put a spacer in here.
            continue;
        }
        var button = $('<button/>');
        button.addClass('ui-button ui-widget ui-state-default ui-corner-all ' +
                        'ui-button-icon-only');
        button.attr('role', 'button');
        button.attr('aria-disabled', 'false');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);

        var icon_img = $('<span/>');
        icon_img.addClass('ui-button-icon-primary ui-icon');
        icon_img.addClass(image);
        icon_img.addClass('ui-corner-all');

        var tooltip_span = $('<span/>');
        tooltip_span.addClass('ui-button-text');
        tooltip_span.html(tooltip);

        button.append(icon_img);
        button.append(tooltip_span);

        nav_element.append(button);
    }

    var fmt_picker_span = $('<span/>');

    var fmt_picker = $('<select/>');
    fmt_picker.addClass('mpl-toolbar-option ui-widget ui-widget-content');
    fmt_picker_span.append(fmt_picker);
    nav_element.append(fmt_picker_span);
    this.format_dropdown = fmt_picker[0];

    for (var ind in mpl.extensions) {
        var fmt = mpl.extensions[ind];
        var option = $(
            '<option/>', {selected: fmt === mpl.default_extension}).html(fmt);
        fmt_picker.append(option)
    }

    // Add hover states to the ui-buttons
    $( ".ui-button" ).hover(
        function() { $(this).addClass("ui-state-hover");},
        function() { $(this).removeClass("ui-state-hover");}
    );

    var status_bar = $('<span class="mpl-message"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];
}

mpl.figure.prototype.request_resize = function(x_pixels, y_pixels) {
    // Request matplotlib to resize the figure. Matplotlib will then trigger a resize in the client,
    // which will in turn request a refresh of the image.
    this.send_message('resize', {'width': x_pixels, 'height': y_pixels});
}

mpl.figure.prototype.send_message = function(type, properties) {
    properties['type'] = type;
    properties['figure_id'] = this.id;
    this.ws.send(JSON.stringify(properties));
}

mpl.figure.prototype.send_draw_message = function() {
    if (!this.waiting) {
        this.waiting = true;
        this.ws.send(JSON.stringify({type: "draw", figure_id: this.id}));
    }
}


mpl.figure.prototype.handle_save = function(fig, msg) {
    var format_dropdown = fig.format_dropdown;
    var format = format_dropdown.options[format_dropdown.selectedIndex].value;
    fig.ondownload(fig, format);
}


mpl.figure.prototype.handle_resize = function(fig, msg) {
    var size = msg['size'];
    if (size[0] != fig.canvas.width || size[1] != fig.canvas.height) {
        fig._resize_canvas(size[0], size[1]);
        fig.send_message("refresh", {});
    };
}

mpl.figure.prototype.handle_rubberband = function(fig, msg) {
    var x0 = msg['x0'];
    var y0 = fig.canvas.height - msg['y0'];
    var x1 = msg['x1'];
    var y1 = fig.canvas.height - msg['y1'];
    x0 = Math.floor(x0) + 0.5;
    y0 = Math.floor(y0) + 0.5;
    x1 = Math.floor(x1) + 0.5;
    y1 = Math.floor(y1) + 0.5;
    var min_x = Math.min(x0, x1);
    var min_y = Math.min(y0, y1);
    var width = Math.abs(x1 - x0);
    var height = Math.abs(y1 - y0);

    fig.rubberband_context.clearRect(
        0, 0, fig.canvas.width, fig.canvas.height);

    fig.rubberband_context.strokeRect(min_x, min_y, width, height);
}

mpl.figure.prototype.handle_figure_label = function(fig, msg) {
    // Updates the figure title.
    fig.header.textContent = msg['label'];
}

mpl.figure.prototype.handle_cursor = function(fig, msg) {
    var cursor = msg['cursor'];
    switch(cursor)
    {
    case 0:
        cursor = 'pointer';
        break;
    case 1:
        cursor = 'default';
        break;
    case 2:
        cursor = 'crosshair';
        break;
    case 3:
        cursor = 'move';
        break;
    }
    fig.rubberband_canvas.style.cursor = cursor;
}

mpl.figure.prototype.handle_message = function(fig, msg) {
    fig.message.textContent = msg['message'];
}

mpl.figure.prototype.handle_draw = function(fig, msg) {
    // Request the server to send over a new figure.
    fig.send_draw_message();
}

mpl.figure.prototype.handle_image_mode = function(fig, msg) {
    fig.image_mode = msg['mode'];
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Called whenever the canvas gets updated.
    this.send_message("ack", {});
}

// A function to construct a web socket function for onmessage handling.
// Called in the figure constructor.
mpl.figure.prototype._make_on_message_function = function(fig) {
    return function socket_on_message(evt) {
        if (evt.data instanceof Blob) {
            /* FIXME: We get "Resource interpreted as Image but
             * transferred with MIME type text/plain:" errors on
             * Chrome.  But how to set the MIME type?  It doesn't seem
             * to be part of the websocket stream */
            evt.data.type = "image/png";

            /* Free the memory for the previous frames */
            if (fig.imageObj.src) {
                (window.URL || window.webkitURL).revokeObjectURL(
                    fig.imageObj.src);
            }

            fig.imageObj.src = (window.URL || window.webkitURL).createObjectURL(
                evt.data);
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }
        else if (typeof evt.data === 'string' && evt.data.slice(0, 21) == "data:image/png;base64") {
            fig.imageObj.src = evt.data;
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }

        var msg = JSON.parse(evt.data);
        var msg_type = msg['type'];

        // Call the  "handle_{type}" callback, which takes
        // the figure and JSON message as its only arguments.
        try {
            var callback = fig["handle_" + msg_type];
        } catch (e) {
            console.log("No handler for the '" + msg_type + "' message type: ", msg);
            return;
        }

        if (callback) {
            try {
                // console.log("Handling '" + msg_type + "' message: ", msg);
                callback(fig, msg);
            } catch (e) {
                console.log("Exception inside the 'handler_" + msg_type + "' callback:", e, e.stack, msg);
            }
        }
    };
}

// from http://stackoverflow.com/questions/1114465/getting-mouse-location-in-canvas
mpl.findpos = function(e) {
    //this section is from http://www.quirksmode.org/js/events_properties.html
    var targ;
    if (!e)
        e = window.event;
    if (e.target)
        targ = e.target;
    else if (e.srcElement)
        targ = e.srcElement;
    if (targ.nodeType == 3) // defeat Safari bug
        targ = targ.parentNode;

    // jQuery normalizes the pageX and pageY
    // pageX,Y are the mouse positions relative to the document
    // offset() returns the position of the element relative to the document
    var x = e.pageX - $(targ).offset().left;
    var y = e.pageY - $(targ).offset().top;

    return {"x": x, "y": y};
};

/*
 * return a copy of an object with only non-object keys
 * we need this to avoid circular references
 * http://stackoverflow.com/a/24161582/3208463
 */
function simpleKeys (original) {
  return Object.keys(original).reduce(function (obj, key) {
    if (typeof original[key] !== 'object')
        obj[key] = original[key]
    return obj;
  }, {});
}

mpl.figure.prototype.mouse_event = function(event, name) {
    var canvas_pos = mpl.findpos(event)

    if (name === 'button_press')
    {
        this.canvas.focus();
        this.canvas_div.focus();
    }

    var x = canvas_pos.x;
    var y = canvas_pos.y;

    this.send_message(name, {x: x, y: y, button: event.button,
                             step: event.step,
                             guiEvent: simpleKeys(event)});

    /* This prevents the web browser from automatically changing to
     * the text insertion cursor when the button is pressed.  We want
     * to control all of the cursor setting manually through the
     * 'cursor' event from matplotlib */
    event.preventDefault();
    return false;
}

mpl.figure.prototype._key_event_extra = function(event, name) {
    // Handle any extra behaviour associated with a key event
}

mpl.figure.prototype.key_event = function(event, name) {

    // Prevent repeat events
    if (name == 'key_press')
    {
        if (event.which === this._key)
            return;
        else
            this._key = event.which;
    }
    if (name == 'key_release')
        this._key = null;

    var value = '';
    if (event.ctrlKey && event.which != 17)
        value += "ctrl+";
    if (event.altKey && event.which != 18)
        value += "alt+";
    if (event.shiftKey && event.which != 16)
        value += "shift+";

    value += 'k';
    value += event.which.toString();

    this._key_event_extra(event, name);

    this.send_message(name, {key: value,
                             guiEvent: simpleKeys(event)});
    return false;
}

mpl.figure.prototype.toolbar_button_onclick = function(name) {
    if (name == 'download') {
        this.handle_save(this, null);
    } else {
        this.send_message("toolbar_button", {name: name});
    }
};

mpl.figure.prototype.toolbar_button_onmouseover = function(tooltip) {
    this.message.textContent = tooltip;
};
mpl.toolbar_items = [["Home", "Reset original view", "fa fa-home icon-home", "home"], ["Back", "Back to  previous view", "fa fa-arrow-left icon-arrow-left", "back"], ["Forward", "Forward to next view", "fa fa-arrow-right icon-arrow-right", "forward"], ["", "", "", ""], ["Pan", "Pan axes with left mouse, zoom with right", "fa fa-arrows icon-move", "pan"], ["Zoom", "Zoom to rectangle", "fa fa-square-o icon-check-empty", "zoom"], ["", "", "", ""], ["Download", "Download plot", "fa fa-floppy-o icon-save", "download"]];

mpl.extensions = ["eps", "jpeg", "pdf", "png", "ps", "raw", "svg", "tif"];

mpl.default_extension = "png";var comm_websocket_adapter = function(comm) {
    // Create a "websocket"-like object which calls the given IPython comm
    // object with the appropriate methods. Currently this is a non binary
    // socket, so there is still some room for performance tuning.
    var ws = {};

    ws.close = function() {
        comm.close()
    };
    ws.send = function(m) {
        //console.log('sending', m);
        comm.send(m);
    };
    // Register the callback with on_msg.
    comm.on_msg(function(msg) {
        //console.log('receiving', msg['content']['data'], msg);
        // Pass the mpl event to the overriden (by mpl) onmessage function.
        ws.onmessage(msg['content']['data'])
    });
    return ws;
}

mpl.mpl_figure_comm = function(comm, msg) {
    // This is the function which gets called when the mpl process
    // starts-up an IPython Comm through the "matplotlib" channel.

    var id = msg.content.data.id;
    // Get hold of the div created by the display call when the Comm
    // socket was opened in Python.
    var element = $("#" + id);
    var ws_proxy = comm_websocket_adapter(comm)

    function ondownload(figure, format) {
        window.open(figure.imageObj.src);
    }

    var fig = new mpl.figure(id, ws_proxy,
                           ondownload,
                           element.get(0));

    // Call onopen now - mpl needs it, as it is assuming we've passed it a real
    // web socket which is closed, not our websocket->open comm proxy.
    ws_proxy.onopen();

    fig.parent_element = element.get(0);
    fig.cell_info = mpl.find_output_cell("<div id='" + id + "'></div>");
    if (!fig.cell_info) {
        console.error("Failed to find cell for figure", id, fig);
        return;
    }

    var output_index = fig.cell_info[2]
    var cell = fig.cell_info[0];

};

mpl.figure.prototype.handle_close = function(fig, msg) {
    fig.root.unbind('remove')

    // Update the output cell to use the data from the current canvas.
    fig.push_to_output();
    var dataURL = fig.canvas.toDataURL();
    // Re-enable the keyboard manager in IPython - without this line, in FF,
    // the notebook keyboard shortcuts fail.
    IPython.keyboard_manager.enable()
    $(fig.parent_element).html('<img src="' + dataURL + '">');
    fig.close_ws(fig, msg);
}

mpl.figure.prototype.close_ws = function(fig, msg){
    fig.send_message('closing', msg);
    // fig.ws.close()
}

mpl.figure.prototype.push_to_output = function(remove_interactive) {
    // Turn the data on the canvas into data in the output cell.
    var dataURL = this.canvas.toDataURL();
    this.cell_info[1]['text/html'] = '<img src="' + dataURL + '">';
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Tell IPython that the notebook contents must change.
    IPython.notebook.set_dirty(true);
    this.send_message("ack", {});
    var fig = this;
    // Wait a second, then push the new image to the DOM so
    // that it is saved nicely (might be nice to debounce this).
    setTimeout(function () { fig.push_to_output() }, 1000);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items){
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) { continue; };

        var button = $('<button class="btn btn-default" href="#" title="' + name + '"><i class="fa ' + image + ' fa-lg"></i></button>');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);
        nav_element.append(button);
    }

    // Add the status bar.
    var status_bar = $('<span class="mpl-message" style="text-align:right; float: right;"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];

    // Add the close button to the window.
    var buttongrp = $('<div class="btn-group inline pull-right"></div>');
    var button = $('<button class="btn btn-mini btn-primary" href="#" title="Stop Interaction"><i class="fa fa-power-off icon-remove icon-large"></i></button>');
    button.click(function (evt) { fig.handle_close(fig, {}); } );
    button.mouseover('Stop Interaction', toolbar_mouse_event);
    buttongrp.append(button);
    var titlebar = this.root.find($('.ui-dialog-titlebar'));
    titlebar.prepend(buttongrp);
}

mpl.figure.prototype._root_extra_style = function(el){
    var fig = this
    el.on("remove", function(){
	fig.close_ws(fig, {});
    });
}

mpl.figure.prototype._canvas_extra_style = function(el){
    // this is important to make the div 'focusable
    el.attr('tabindex', 0)
    // reach out to IPython and tell the keyboard manager to turn it's self
    // off when our div gets focus

    // location in version 3
    if (IPython.notebook.keyboard_manager) {
        IPython.notebook.keyboard_manager.register_events(el);
    }
    else {
        // location in version 2
        IPython.keyboard_manager.register_events(el);
    }

}

mpl.figure.prototype._key_event_extra = function(event, name) {
    var manager = IPython.notebook.keyboard_manager;
    if (!manager)
        manager = IPython.keyboard_manager;

    // Check for shift+enter
    if (event.shiftKey && event.which == 13) {
        this.canvas_div.blur();
        event.shiftKey = false;
        // Send a "J" for go to next cell
        event.which = 74;
        event.keyCode = 74;
        manager.command_mode();
        manager.handle_keydown(event);
    }
}

mpl.figure.prototype.handle_save = function(fig, msg) {
    fig.ondownload(fig, null);
}


mpl.find_output_cell = function(html_output) {
    // Return the cell and output element which can be found *uniquely* in the notebook.
    // Note - this is a bit hacky, but it is done because the "notebook_saving.Notebook"
    // IPython event is triggered only after the cells have been serialised, which for
    // our purposes (turning an active figure into a static one), is too late.
    var cells = IPython.notebook.get_cells();
    var ncells = cells.length;
    for (var i=0; i<ncells; i++) {
        var cell = cells[i];
        if (cell.cell_type === 'code'){
            for (var j=0; j<cell.output_area.outputs.length; j++) {
                var data = cell.output_area.outputs[j];
                if (data.data) {
                    // IPython >= 3 moved mimebundle to data attribute of output
                    data = data.data;
                }
                if (data['text/html'] == html_output) {
                    return [cell, data, j];
                }
            }
        }
    }
}

// Register the function which deals with the matplotlib target/channel.
// The kernel may be null if the page has been refreshed.
if (IPython.notebook.kernel != null) {
    IPython.notebook.kernel.comm_manager.register_target('matplotlib', mpl.mpl_figure_comm);
}

</script>
</div>

</div>

<div class="output_area"><div class="prompt"></div>

<div class="output_html rendered_html output_subarea ">
<img src="data:image/png;base64,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">
</div>

</div>

<div class="output_area"><div class="prompt output_prompt">Out[16]:</div>


<div class="output_text output_subarea output_execute_result">
<pre>&lt;ggplot: (28862987)&gt;</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>By looking at this plot we can say that people encountered the advertisement mostly between 11 a.m. and 17 p.m.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="B.-Case-Discussion-Questions">B. Case Discussion Questions<a class="anchor-link" href="#B.-Case-Discussion-Questions">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="1.-Was-the-advertising-compaign-effective?-Did-additional-consumers-convert-as-a-result-of-the-ad-campaign?">1. Was the advertising compaign effective? Did additional consumers convert as a result of the ad campaign?<a class="anchor-link" href="#1.-Was-the-advertising-compaign-effective?-Did-additional-consumers-convert-as-a-result-of-the-ad-campaign?">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Rocket Fuel designed the experiment to have two groups; a control group and a test group and each group have a different conversion rate:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># Calculate conversion rates for control and test groups</span>

<span class="n">percent_conversion_control</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)]</span><span class="o">.</span><span class="n">count</span><span class="p">())</span> \
                                 <span class="o">/</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">()</span> <span class="o">*</span> <span class="mi">100</span>
<span class="n">percent_conversion_test</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">][(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">)]</span><span class="o">.</span><span class="n">count</span><span class="p">())</span> \
                              <span class="o">/</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">()</span> <span class="o">*</span> <span class="mi">100</span>

<span class="k">print</span><span class="p">(</span><span class="s">&quot;Conversion rate for the control group (</span><span class="si">%%</span><span class="s"> users who made a purchase): </span><span class="si">%%</span><span class="s"> </span><span class="si">%.2f</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">percent_conversion_control</span>)
<span class="k">print</span><span class="p">(</span><span class="s">&quot;Conversion rate for the test group (</span><span class="si">%%</span><span class="s"> users who made a purchase): </span><span class="si">%%</span><span class="s"> </span><span class="si">%.2f</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">percent_conversion_test</span>)
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Conversion rate for the control group (% users who made a purchase): % 1.79
Conversion rate for the test group (% users who made a purchase): % 2.55
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>In order to analyze the effectiveness of the advertisement campaign we can conduct a hypothesis test and examine whether there is a statistically significant difference between these two proportions.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># Calculate group size:</span>
<span class="n">n_test</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">()</span>
<span class="n">n_control</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">()</span>

<span class="k">print</span> <span class="s">&quot;n_test: &quot;</span><span class="p">,</span> <span class="n">n_test</span>
<span class="k">print</span> <span class="s">&quot;n_control&quot;</span><span class="p">,</span> <span class="n">n_control</span>

<span class="c"># Calculate total number of converted users in each group:</span>
<span class="n">y_test</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">])</span>
<span class="n">y_control</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">])</span>

<span class="k">print</span> <span class="s">&quot;y_test: &quot;</span><span class="p">,</span> <span class="n">y_test</span>
<span class="k">print</span> <span class="s">&quot;y_control&quot;</span><span class="p">,</span> <span class="n">y_control</span>

<span class="c"># Calculate conversion rates for each group:</span>
<span class="n">p_test</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">y_test</span><span class="p">)</span> <span class="o">/</span> <span class="n">n_test</span>
<span class="n">p_control</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">y_control</span><span class="p">)</span> <span class="o">/</span> <span class="n">n_control</span>

<span class="n">p_hat</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">y_test</span> <span class="o">+</span> <span class="n">y_control</span><span class="p">)</span> <span class="o">/</span> <span class="p">(</span><span class="n">n_test</span> <span class="o">+</span> <span class="n">n_control</span><span class="p">)</span>

<span class="k">print</span> <span class="s">&quot;p_test: &quot;</span><span class="p">,</span> <span class="n">p_test</span>
<span class="k">print</span> <span class="s">&quot;p_control: &quot;</span><span class="p">,</span> <span class="n">p_control</span>
<span class="k">print</span> <span class="s">&quot;p_hat: &quot;</span><span class="p">,</span> <span class="n">p_hat</span>

<span class="c"># Define null and alternative hypothesis:</span>
<span class="k">print</span> <span class="s">&quot;H0: p_test = p_control&quot;</span>
<span class="k">print</span> <span class="s">&quot;HA: p_test &gt; p_control&quot;</span>

<span class="c"># Calculate z-statistic:</span>
<span class="n">z_stat</span> <span class="o">=</span> <span class="p">(</span><span class="n">p_test</span> <span class="o">-</span> <span class="n">p_control</span><span class="p">)</span> <span class="o">/</span> <span class="n">math</span><span class="o">.</span><span class="n">sqrt</span><span class="p">(</span><span class="n">p_hat</span> <span class="o">*</span> <span class="p">(</span><span class="mi">1</span> <span class="o">-</span> <span class="n">p_hat</span><span class="p">)</span> <span class="o">*</span> <span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="mi">1</span><span class="p">)</span> <span class="o">/</span> <span class="n">n_test</span> <span class="o">+</span> <span class="nb">float</span><span class="p">(</span><span class="mi">1</span><span class="p">)</span> <span class="o">/</span> <span class="n">n_control</span><span class="p">))</span>

<span class="k">print</span> <span class="s">&quot;z_stat: &quot;</span><span class="p">,</span> <span class="n">z_stat</span>

<span class="c"># Calculate z-critical value:</span>
<span class="n">alpha</span> <span class="o">=</span> <span class="mf">0.05</span>
<span class="n">z_crit</span> <span class="o">=</span> <span class="n">scipy</span><span class="o">.</span><span class="n">stats</span><span class="o">.</span><span class="n">norm</span><span class="o">.</span><span class="n">ppf</span><span class="p">(</span><span class="mi">1</span><span class="o">-</span><span class="n">alpha</span><span class="p">)</span>

<span class="k">print</span> <span class="s">&quot;z_crit: &quot;</span><span class="p">,</span> <span class="n">z_crit</span>


<span class="c"># Conclude results:</span>
<span class="k">if</span> <span class="nb">abs</span><span class="p">(</span><span class="n">z_stat</span><span class="p">)</span> <span class="o">&gt;</span> <span class="n">z_crit</span><span class="p">:</span>
    <span class="k">print</span> <span class="s">&quot;Result: Reject H0&quot;</span>
    <span class="k">print</span> <span class="s">&quot;With a 95</span><span class="si">% c</span><span class="s">onfidence level, conversion rate for test group is bigger than control group.&quot;</span>
<span class="k">else</span><span class="p">:</span>
    <span class="k">print</span> <span class="s">&quot;Result: Not enough evidence to reject H0&quot;</span>
    <span class="k">print</span> <span class="s">&quot;With a 95</span><span class="si">% c</span><span class="s">onfidence level, conversion rate for both groups are the same.&quot;</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>n_test:  564577
n_control 23524
y_test:  14423
y_control 420
p_test:  0.0255465596367
p_control:  0.0178541064445
p_hat:  0.0252388620322
H0: p_test = p_control
HA: p_test &gt; p_control
z_stat:  7.37007812655
z_crit:  1.64485362695
Result: Reject H0
With a 95% confidence level, conversion rate for test group is bigger than control group.
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>According to above calculations, with a 95% level of significance, conversion rates for test group, that actually saw the advertisement, is higher than control group. We can conclude that the advertisement campaign actually workes. Two populations are different and more people buys the TaskaBella's handbag after seing the online advertisement than people who buys the handbag after seing a public service announcement.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="2.-Was-the-campaign-profitable?">2. Was the campaign profitable?<a class="anchor-link" href="#2.-Was-the-campaign-profitable?">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>a. How much more money did TeskaBella make by running the campaign (excluding advertising costs)?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Since TaskaBella has a strong presence in the social media, we can assume that all of the converted users in the control group, who saw a public service announcement, bought the handbag because of the word-of-mouth effect and all converted users in the test group bought the handbag because of the online advertisement campaign, then TaskaBella's revenue is:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre> <span class="c"># Calculate TaskaBella&#39;s revenue by running the campaign:</span>
<span class="n">test_group_converted_users</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">])</span>
<span class="n">each_converted_user_worth</span> <span class="o">=</span> <span class="mi">40</span>
<span class="n">revenue_from_ad_campaign</span> <span class="o">=</span> <span class="n">each_converted_user_worth</span> <span class="o">*</span> <span class="n">test_group_converted_users</span>

<span class="k">print</span>  <span class="s">&quot;Total number of converted users in test group: &quot;</span><span class="p">,</span> <span class="n">test_group_converted_users</span>
<span class="k">print</span><span class="p">(</span><span class="s">&quot;Each converted user is worth $</span><span class="si">%d</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">each_converted_user_worth</span>)
<span class="k">print</span><span class="p">(</span><span class="s">&quot;TeskaBella made $</span><span class="si">%d</span><span class="s"> by running the ad campaign.&quot;</span> <span class="o">%</span><span class="k">revenue_from_ad_campaign</span>)
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Total number of converted users in test group:  14423
Each converted user is worth $40
TeskaBella made $576920 by running the ad campaign.
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># Calculate word-of-mouth effect (total number of converted users in the control group):</span>
<span class="n">control_group_converted_users</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">])</span>

<span class="k">print</span><span class="p">(</span><span class="s">&quot;By calculating so, we assume that </span><span class="si">%d</span><span class="s"> control group users bought the handbag because of word-of-mouth effect.&quot;</span> \
      <span class="o">%</span><span class="k">control_group_converted_users</span>)
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>By calculating so, we assume that 420 control group users bought the handbag because of word-of-mouth effect.
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>b. What was the cost of the campaign?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># Calculate advertising campaign cost</span>
<span class="n">cost_of_campaign</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">])</span> <span class="o">/</span> <span class="mi">1000</span> <span class="o">*</span> <span class="mi">9</span>

<span class="k">print</span> <span class="s">&quot;Total number of impressions: &quot;</span><span class="p">,</span> <span class="nb">sum</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">])</span>
<span class="k">print</span> <span class="s">&quot;Cost per thousand impressions: $&quot;</span><span class="p">,</span> <span class="mi">9</span>
<span class="k">print</span><span class="p">(</span><span class="s">&quot;Advertisement campaign cost: $</span><span class="si">%d</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">cost_of_campaign</span>)
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Total number of impressions:  14597182
Cost per thousand impressions: $ 9
Advertisement campaign cost: $131373
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>c. Calculate the ROI of the campaign. Was the campaign profitable?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># Calculate the ROI of the ad campaign</span>
<span class="n">roi</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">revenue_from_ad_campaign</span> <span class="o">-</span> <span class="n">cost_of_campaign</span><span class="p">)</span> <span class="o">/</span> <span class="n">cost_of_campaign</span> <span class="o">*</span> <span class="mi">100</span>
<span class="k">print</span> <span class="s">&quot;ROI of the advertisement campaign was %&quot;</span><span class="p">,</span> <span class="n">roi</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>ROI of the advertisement campaign was % 339.146552183
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>%339 is a very high return on investment and means that each dollar TaskaBella spent on advertising campaign, TaskaBella earned $3.39. So we can say that this advertisement campaign was profitable.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>d. What was the opportunity cost of including a control group; how much more could have TaskaBella made with a smaller control group or not having a control group at all?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>If we assume that the conversion rates for control and test groups won't change when we decrease the control group size:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[23]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># Do revenue calculations for 3, 2, 1 and 0 % control groups</span>
<span class="n">overall_size</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;user_id&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">()</span>
<span class="n">original_control_group_size</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;user_id&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">()</span>
<span class="n">overall_conversion_rate</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">])</span> <span class="o">/</span> <span class="nb">float</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">())</span>
<span class="n">control_conversion_rate</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">])</span> <span class="o">/</span> <span class="nb">float</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">())</span>
<span class="n">test_conversion_rate</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">])</span> <span class="o">/</span> <span class="nb">float</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">())</span>

<span class="n">k_values</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">revenues</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">opportunities_lost</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">print</span> <span class="s">&quot;Overall size: &quot;</span><span class="p">,</span> <span class="n">overall_size</span>
<span class="k">print</span> <span class="s">&quot;Original control group size: &quot;</span><span class="p">,</span> <span class="n">original_control_group_size</span>
<span class="k">print</span> <span class="s">&quot;Test group conversion rate: &quot;</span><span class="p">,</span> <span class="n">test_conversion_rate</span>
<span class="k">print</span> <span class="s">&quot;----------------------------------------------&quot;</span>

<span class="k">for</span> <span class="n">k</span> <span class="ow">in</span> <span class="nb">reversed</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">)):</span>
    <span class="n">new_control_group_percent</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">k</span><span class="p">)</span> <span class="o">/</span> <span class="mi">100</span>
    <span class="n">new_control_group_size</span> <span class="o">=</span> <span class="n">overall_size</span> <span class="o">*</span> <span class="n">new_control_group_percent</span>
    <span class="n">control_group_to_test_group</span> <span class="o">=</span> <span class="n">original_control_group_size</span> <span class="o">-</span> <span class="n">new_control_group_size</span>
    <span class="n">new_converted_users</span> <span class="o">=</span> <span class="n">control_group_to_test_group</span> <span class="o">*</span> <span class="n">test_conversion_rate</span>
    <span class="n">opportunity_lost</span> <span class="o">=</span> <span class="mi">40</span> <span class="o">*</span> <span class="n">new_converted_users</span>
    
    <span class="n">k_values</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">k</span><span class="p">)</span>
    <span class="n">opportunities_lost</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">opportunity_lost</span><span class="p">)</span>
    
    <span class="k">print</span> <span class="s">&quot;New control group percent (%): &quot;</span><span class="p">,</span> <span class="n">k</span>
    <span class="k">print</span><span class="p">(</span><span class="s">&quot;New control group size: </span><span class="si">%d</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">new_control_group_size</span>)
    <span class="k">print</span><span class="p">(</span><span class="s">&quot;New converted users coming from control group: </span><span class="si">%d</span><span class="s">&quot;</span> <span class="o">%</span><span class="k">new_converted_users</span>) #Round to nearest integer while printing
    <span class="k">print</span><span class="p">(</span><span class="s">&quot;Opportunity lost (if control group size was </span><span class="si">%%</span><span class="s"> </span><span class="si">%d</span><span class="s">): </span><span class="si">%d</span><span class="s">&quot;</span> <span class="o">%</span><span class="p">(</span><span class="n">k</span><span class="p">,</span> <span class="n">opportunity_lost</span><span class="p">))</span>
    <span class="k">print</span> <span class="s">&quot;----------------------------------------------&quot;</span>

<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">k_values</span><span class="p">,</span> <span class="n">opportunities_lost</span><span class="p">,</span> <span class="s">&#39;ro&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s">&#39;Opportunity Lost&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s">&#39;Control Group Size&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5000</span><span class="p">,</span> <span class="mi">25000</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s">&#39;Opportunities Lost for Different Control Group Sizes&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Overall size:  588101
Original control group size:  23524
Test group conversion rate:  0.0255465596367
----------------------------------------------
New control group percent (%):  3
New control group size: 17643
New converted users coming from control group: 150
Opportunity lost (if control group size was % 3): 6009
----------------------------------------------
New control group percent (%):  2
New control group size: 11762
New converted users coming from control group: 300
Opportunity lost (if control group size was % 2): 12019
----------------------------------------------
New control group percent (%):  1
New control group size: 5881
New converted users coming from control group: 450
Opportunity lost (if control group size was % 1): 18028
----------------------------------------------
New control group percent (%):  0
New control group size: 0
New converted users coming from control group: 600
Opportunity lost (if control group size was % 0): 24038
----------------------------------------------
</pre>
</div>
</div>

<div class="output_area"><div class="prompt"></div>


<div class="output_subarea output_javascript ">
<script type="text/javascript">
/* Put everything inside the global mpl namespace */
window.mpl = {};

mpl.get_websocket_type = function() {
    if (typeof(WebSocket) !== 'undefined') {
        return WebSocket;
    } else if (typeof(MozWebSocket) !== 'undefined') {
        return MozWebSocket;
    } else {
        alert('Your browser does not have WebSocket support.' +
              'Please try Chrome, Safari or Firefox ≥ 6. ' +
              'Firefox 4 and 5 are also supported but you ' +
              'have to enable WebSockets in about:config.');
    };
}

mpl.figure = function(figure_id, websocket, ondownload, parent_element) {
    this.id = figure_id;

    this.ws = websocket;

    this.supports_binary = (this.ws.binaryType != undefined);

    if (!this.supports_binary) {
        var warnings = document.getElementById("mpl-warnings");
        if (warnings) {
            warnings.style.display = 'block';
            warnings.textContent = (
                "This browser does not support binary websocket messages. " +
                    "Performance may be slow.");
        }
    }

    this.imageObj = new Image();

    this.context = undefined;
    this.message = undefined;
    this.canvas = undefined;
    this.rubberband_canvas = undefined;
    this.rubberband_context = undefined;
    this.format_dropdown = undefined;

    this.image_mode = 'full';

    this.root = $('<div/>');
    this._root_extra_style(this.root)
    this.root.attr('style', 'display: inline-block');

    $(parent_element).append(this.root);

    this._init_header(this);
    this._init_canvas(this);
    this._init_toolbar(this);

    var fig = this;

    this.waiting = false;

    this.ws.onopen =  function () {
            fig.send_message("supports_binary", {value: fig.supports_binary});
            fig.send_message("send_image_mode", {});
            fig.send_message("refresh", {});
        }

    this.imageObj.onload = function() {
            if (fig.image_mode == 'full') {
                // Full images could contain transparency (where diff images
                // almost always do), so we need to clear the canvas so that
                // there is no ghosting.
                fig.context.clearRect(0, 0, fig.canvas.width, fig.canvas.height);
            }
            fig.context.drawImage(fig.imageObj, 0, 0);
        };

    this.imageObj.onunload = function() {
        this.ws.close();
    }

    this.ws.onmessage = this._make_on_message_function(this);

    this.ondownload = ondownload;
}

mpl.figure.prototype._init_header = function() {
    var titlebar = $(
        '<div class="ui-dialog-titlebar ui-widget-header ui-corner-all ' +
        'ui-helper-clearfix"/>');
    var titletext = $(
        '<div class="ui-dialog-title" style="width: 100%; ' +
        'text-align: center; padding: 3px;"/>');
    titlebar.append(titletext)
    this.root.append(titlebar);
    this.header = titletext[0];
}



mpl.figure.prototype._canvas_extra_style = function(canvas_div) {

}


mpl.figure.prototype._root_extra_style = function(canvas_div) {

}

mpl.figure.prototype._init_canvas = function() {
    var fig = this;

    var canvas_div = $('<div/>');

    canvas_div.attr('style', 'position: relative; clear: both; outline: 0');

    function canvas_keyboard_event(event) {
        return fig.key_event(event, event['data']);
    }

    canvas_div.keydown('key_press', canvas_keyboard_event);
    canvas_div.keyup('key_release', canvas_keyboard_event);
    this.canvas_div = canvas_div
    this._canvas_extra_style(canvas_div)
    this.root.append(canvas_div);

    var canvas = $('<canvas/>');
    canvas.addClass('mpl-canvas');
    canvas.attr('style', "left: 0; top: 0; z-index: 0; outline: 0")

    this.canvas = canvas[0];
    this.context = canvas[0].getContext("2d");

    var rubberband = $('<canvas/>');
    rubberband.attr('style', "position: absolute; left: 0; top: 0; z-index: 1;")

    var pass_mouse_events = true;

    canvas_div.resizable({
        start: function(event, ui) {
            pass_mouse_events = false;
        },
        resize: function(event, ui) {
            fig.request_resize(ui.size.width, ui.size.height);
        },
        stop: function(event, ui) {
            pass_mouse_events = true;
            fig.request_resize(ui.size.width, ui.size.height);
        },
    });

    function mouse_event_fn(event) {
        if (pass_mouse_events)
            return fig.mouse_event(event, event['data']);
    }

    rubberband.mousedown('button_press', mouse_event_fn);
    rubberband.mouseup('button_release', mouse_event_fn);
    // Throttle sequential mouse events to 1 every 20ms.
    rubberband.mousemove('motion_notify', mouse_event_fn);

    rubberband.mouseenter('figure_enter', mouse_event_fn);
    rubberband.mouseleave('figure_leave', mouse_event_fn);

    canvas_div.on("wheel", function (event) {
        event = event.originalEvent;
        event['data'] = 'scroll'
        if (event.deltaY < 0) {
            event.step = 1;
        } else {
            event.step = -1;
        }
        mouse_event_fn(event);
    });

    canvas_div.append(canvas);
    canvas_div.append(rubberband);

    this.rubberband = rubberband;
    this.rubberband_canvas = rubberband[0];
    this.rubberband_context = rubberband[0].getContext("2d");
    this.rubberband_context.strokeStyle = "#000000";

    this._resize_canvas = function(width, height) {
        // Keep the size of the canvas, canvas container, and rubber band
        // canvas in synch.
        canvas_div.css('width', width)
        canvas_div.css('height', height)

        canvas.attr('width', width);
        canvas.attr('height', height);

        rubberband.attr('width', width);
        rubberband.attr('height', height);
    }

    // Set the figure to an initial 600x600px, this will subsequently be updated
    // upon first draw.
    this._resize_canvas(600, 600);

    // Disable right mouse context menu.
    $(this.rubberband_canvas).bind("contextmenu",function(e){
        return false;
    });

    function set_focus () {
        canvas.focus();
        canvas_div.focus();
    }

    window.setTimeout(set_focus, 100);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items) {
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) {
            // put a spacer in here.
            continue;
        }
        var button = $('<button/>');
        button.addClass('ui-button ui-widget ui-state-default ui-corner-all ' +
                        'ui-button-icon-only');
        button.attr('role', 'button');
        button.attr('aria-disabled', 'false');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);

        var icon_img = $('<span/>');
        icon_img.addClass('ui-button-icon-primary ui-icon');
        icon_img.addClass(image);
        icon_img.addClass('ui-corner-all');

        var tooltip_span = $('<span/>');
        tooltip_span.addClass('ui-button-text');
        tooltip_span.html(tooltip);

        button.append(icon_img);
        button.append(tooltip_span);

        nav_element.append(button);
    }

    var fmt_picker_span = $('<span/>');

    var fmt_picker = $('<select/>');
    fmt_picker.addClass('mpl-toolbar-option ui-widget ui-widget-content');
    fmt_picker_span.append(fmt_picker);
    nav_element.append(fmt_picker_span);
    this.format_dropdown = fmt_picker[0];

    for (var ind in mpl.extensions) {
        var fmt = mpl.extensions[ind];
        var option = $(
            '<option/>', {selected: fmt === mpl.default_extension}).html(fmt);
        fmt_picker.append(option)
    }

    // Add hover states to the ui-buttons
    $( ".ui-button" ).hover(
        function() { $(this).addClass("ui-state-hover");},
        function() { $(this).removeClass("ui-state-hover");}
    );

    var status_bar = $('<span class="mpl-message"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];
}

mpl.figure.prototype.request_resize = function(x_pixels, y_pixels) {
    // Request matplotlib to resize the figure. Matplotlib will then trigger a resize in the client,
    // which will in turn request a refresh of the image.
    this.send_message('resize', {'width': x_pixels, 'height': y_pixels});
}

mpl.figure.prototype.send_message = function(type, properties) {
    properties['type'] = type;
    properties['figure_id'] = this.id;
    this.ws.send(JSON.stringify(properties));
}

mpl.figure.prototype.send_draw_message = function() {
    if (!this.waiting) {
        this.waiting = true;
        this.ws.send(JSON.stringify({type: "draw", figure_id: this.id}));
    }
}


mpl.figure.prototype.handle_save = function(fig, msg) {
    var format_dropdown = fig.format_dropdown;
    var format = format_dropdown.options[format_dropdown.selectedIndex].value;
    fig.ondownload(fig, format);
}


mpl.figure.prototype.handle_resize = function(fig, msg) {
    var size = msg['size'];
    if (size[0] != fig.canvas.width || size[1] != fig.canvas.height) {
        fig._resize_canvas(size[0], size[1]);
        fig.send_message("refresh", {});
    };
}

mpl.figure.prototype.handle_rubberband = function(fig, msg) {
    var x0 = msg['x0'];
    var y0 = fig.canvas.height - msg['y0'];
    var x1 = msg['x1'];
    var y1 = fig.canvas.height - msg['y1'];
    x0 = Math.floor(x0) + 0.5;
    y0 = Math.floor(y0) + 0.5;
    x1 = Math.floor(x1) + 0.5;
    y1 = Math.floor(y1) + 0.5;
    var min_x = Math.min(x0, x1);
    var min_y = Math.min(y0, y1);
    var width = Math.abs(x1 - x0);
    var height = Math.abs(y1 - y0);

    fig.rubberband_context.clearRect(
        0, 0, fig.canvas.width, fig.canvas.height);

    fig.rubberband_context.strokeRect(min_x, min_y, width, height);
}

mpl.figure.prototype.handle_figure_label = function(fig, msg) {
    // Updates the figure title.
    fig.header.textContent = msg['label'];
}

mpl.figure.prototype.handle_cursor = function(fig, msg) {
    var cursor = msg['cursor'];
    switch(cursor)
    {
    case 0:
        cursor = 'pointer';
        break;
    case 1:
        cursor = 'default';
        break;
    case 2:
        cursor = 'crosshair';
        break;
    case 3:
        cursor = 'move';
        break;
    }
    fig.rubberband_canvas.style.cursor = cursor;
}

mpl.figure.prototype.handle_message = function(fig, msg) {
    fig.message.textContent = msg['message'];
}

mpl.figure.prototype.handle_draw = function(fig, msg) {
    // Request the server to send over a new figure.
    fig.send_draw_message();
}

mpl.figure.prototype.handle_image_mode = function(fig, msg) {
    fig.image_mode = msg['mode'];
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Called whenever the canvas gets updated.
    this.send_message("ack", {});
}

// A function to construct a web socket function for onmessage handling.
// Called in the figure constructor.
mpl.figure.prototype._make_on_message_function = function(fig) {
    return function socket_on_message(evt) {
        if (evt.data instanceof Blob) {
            /* FIXME: We get "Resource interpreted as Image but
             * transferred with MIME type text/plain:" errors on
             * Chrome.  But how to set the MIME type?  It doesn't seem
             * to be part of the websocket stream */
            evt.data.type = "image/png";

            /* Free the memory for the previous frames */
            if (fig.imageObj.src) {
                (window.URL || window.webkitURL).revokeObjectURL(
                    fig.imageObj.src);
            }

            fig.imageObj.src = (window.URL || window.webkitURL).createObjectURL(
                evt.data);
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }
        else if (typeof evt.data === 'string' && evt.data.slice(0, 21) == "data:image/png;base64") {
            fig.imageObj.src = evt.data;
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }

        var msg = JSON.parse(evt.data);
        var msg_type = msg['type'];

        // Call the  "handle_{type}" callback, which takes
        // the figure and JSON message as its only arguments.
        try {
            var callback = fig["handle_" + msg_type];
        } catch (e) {
            console.log("No handler for the '" + msg_type + "' message type: ", msg);
            return;
        }

        if (callback) {
            try {
                // console.log("Handling '" + msg_type + "' message: ", msg);
                callback(fig, msg);
            } catch (e) {
                console.log("Exception inside the 'handler_" + msg_type + "' callback:", e, e.stack, msg);
            }
        }
    };
}

// from http://stackoverflow.com/questions/1114465/getting-mouse-location-in-canvas
mpl.findpos = function(e) {
    //this section is from http://www.quirksmode.org/js/events_properties.html
    var targ;
    if (!e)
        e = window.event;
    if (e.target)
        targ = e.target;
    else if (e.srcElement)
        targ = e.srcElement;
    if (targ.nodeType == 3) // defeat Safari bug
        targ = targ.parentNode;

    // jQuery normalizes the pageX and pageY
    // pageX,Y are the mouse positions relative to the document
    // offset() returns the position of the element relative to the document
    var x = e.pageX - $(targ).offset().left;
    var y = e.pageY - $(targ).offset().top;

    return {"x": x, "y": y};
};

/*
 * return a copy of an object with only non-object keys
 * we need this to avoid circular references
 * http://stackoverflow.com/a/24161582/3208463
 */
function simpleKeys (original) {
  return Object.keys(original).reduce(function (obj, key) {
    if (typeof original[key] !== 'object')
        obj[key] = original[key]
    return obj;
  }, {});
}

mpl.figure.prototype.mouse_event = function(event, name) {
    var canvas_pos = mpl.findpos(event)

    if (name === 'button_press')
    {
        this.canvas.focus();
        this.canvas_div.focus();
    }

    var x = canvas_pos.x;
    var y = canvas_pos.y;

    this.send_message(name, {x: x, y: y, button: event.button,
                             step: event.step,
                             guiEvent: simpleKeys(event)});

    /* This prevents the web browser from automatically changing to
     * the text insertion cursor when the button is pressed.  We want
     * to control all of the cursor setting manually through the
     * 'cursor' event from matplotlib */
    event.preventDefault();
    return false;
}

mpl.figure.prototype._key_event_extra = function(event, name) {
    // Handle any extra behaviour associated with a key event
}

mpl.figure.prototype.key_event = function(event, name) {

    // Prevent repeat events
    if (name == 'key_press')
    {
        if (event.which === this._key)
            return;
        else
            this._key = event.which;
    }
    if (name == 'key_release')
        this._key = null;

    var value = '';
    if (event.ctrlKey && event.which != 17)
        value += "ctrl+";
    if (event.altKey && event.which != 18)
        value += "alt+";
    if (event.shiftKey && event.which != 16)
        value += "shift+";

    value += 'k';
    value += event.which.toString();

    this._key_event_extra(event, name);

    this.send_message(name, {key: value,
                             guiEvent: simpleKeys(event)});
    return false;
}

mpl.figure.prototype.toolbar_button_onclick = function(name) {
    if (name == 'download') {
        this.handle_save(this, null);
    } else {
        this.send_message("toolbar_button", {name: name});
    }
};

mpl.figure.prototype.toolbar_button_onmouseover = function(tooltip) {
    this.message.textContent = tooltip;
};
mpl.toolbar_items = [["Home", "Reset original view", "fa fa-home icon-home", "home"], ["Back", "Back to  previous view", "fa fa-arrow-left icon-arrow-left", "back"], ["Forward", "Forward to next view", "fa fa-arrow-right icon-arrow-right", "forward"], ["", "", "", ""], ["Pan", "Pan axes with left mouse, zoom with right", "fa fa-arrows icon-move", "pan"], ["Zoom", "Zoom to rectangle", "fa fa-square-o icon-check-empty", "zoom"], ["", "", "", ""], ["Download", "Download plot", "fa fa-floppy-o icon-save", "download"]];

mpl.extensions = ["eps", "jpeg", "pdf", "png", "ps", "raw", "svg", "tif"];

mpl.default_extension = "png";var comm_websocket_adapter = function(comm) {
    // Create a "websocket"-like object which calls the given IPython comm
    // object with the appropriate methods. Currently this is a non binary
    // socket, so there is still some room for performance tuning.
    var ws = {};

    ws.close = function() {
        comm.close()
    };
    ws.send = function(m) {
        //console.log('sending', m);
        comm.send(m);
    };
    // Register the callback with on_msg.
    comm.on_msg(function(msg) {
        //console.log('receiving', msg['content']['data'], msg);
        // Pass the mpl event to the overriden (by mpl) onmessage function.
        ws.onmessage(msg['content']['data'])
    });
    return ws;
}

mpl.mpl_figure_comm = function(comm, msg) {
    // This is the function which gets called when the mpl process
    // starts-up an IPython Comm through the "matplotlib" channel.

    var id = msg.content.data.id;
    // Get hold of the div created by the display call when the Comm
    // socket was opened in Python.
    var element = $("#" + id);
    var ws_proxy = comm_websocket_adapter(comm)

    function ondownload(figure, format) {
        window.open(figure.imageObj.src);
    }

    var fig = new mpl.figure(id, ws_proxy,
                           ondownload,
                           element.get(0));

    // Call onopen now - mpl needs it, as it is assuming we've passed it a real
    // web socket which is closed, not our websocket->open comm proxy.
    ws_proxy.onopen();

    fig.parent_element = element.get(0);
    fig.cell_info = mpl.find_output_cell("<div id='" + id + "'></div>");
    if (!fig.cell_info) {
        console.error("Failed to find cell for figure", id, fig);
        return;
    }

    var output_index = fig.cell_info[2]
    var cell = fig.cell_info[0];

};

mpl.figure.prototype.handle_close = function(fig, msg) {
    fig.root.unbind('remove')

    // Update the output cell to use the data from the current canvas.
    fig.push_to_output();
    var dataURL = fig.canvas.toDataURL();
    // Re-enable the keyboard manager in IPython - without this line, in FF,
    // the notebook keyboard shortcuts fail.
    IPython.keyboard_manager.enable()
    $(fig.parent_element).html('<img src="' + dataURL + '">');
    fig.close_ws(fig, msg);
}

mpl.figure.prototype.close_ws = function(fig, msg){
    fig.send_message('closing', msg);
    // fig.ws.close()
}

mpl.figure.prototype.push_to_output = function(remove_interactive) {
    // Turn the data on the canvas into data in the output cell.
    var dataURL = this.canvas.toDataURL();
    this.cell_info[1]['text/html'] = '<img src="' + dataURL + '">';
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Tell IPython that the notebook contents must change.
    IPython.notebook.set_dirty(true);
    this.send_message("ack", {});
    var fig = this;
    // Wait a second, then push the new image to the DOM so
    // that it is saved nicely (might be nice to debounce this).
    setTimeout(function () { fig.push_to_output() }, 1000);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items){
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) { continue; };

        var button = $('<button class="btn btn-default" href="#" title="' + name + '"><i class="fa ' + image + ' fa-lg"></i></button>');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);
        nav_element.append(button);
    }

    // Add the status bar.
    var status_bar = $('<span class="mpl-message" style="text-align:right; float: right;"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];

    // Add the close button to the window.
    var buttongrp = $('<div class="btn-group inline pull-right"></div>');
    var button = $('<button class="btn btn-mini btn-primary" href="#" title="Stop Interaction"><i class="fa fa-power-off icon-remove icon-large"></i></button>');
    button.click(function (evt) { fig.handle_close(fig, {}); } );
    button.mouseover('Stop Interaction', toolbar_mouse_event);
    buttongrp.append(button);
    var titlebar = this.root.find($('.ui-dialog-titlebar'));
    titlebar.prepend(buttongrp);
}

mpl.figure.prototype._root_extra_style = function(el){
    var fig = this
    el.on("remove", function(){
	fig.close_ws(fig, {});
    });
}

mpl.figure.prototype._canvas_extra_style = function(el){
    // this is important to make the div 'focusable
    el.attr('tabindex', 0)
    // reach out to IPython and tell the keyboard manager to turn it's self
    // off when our div gets focus

    // location in version 3
    if (IPython.notebook.keyboard_manager) {
        IPython.notebook.keyboard_manager.register_events(el);
    }
    else {
        // location in version 2
        IPython.keyboard_manager.register_events(el);
    }

}

mpl.figure.prototype._key_event_extra = function(event, name) {
    var manager = IPython.notebook.keyboard_manager;
    if (!manager)
        manager = IPython.keyboard_manager;

    // Check for shift+enter
    if (event.shiftKey && event.which == 13) {
        this.canvas_div.blur();
        event.shiftKey = false;
        // Send a "J" for go to next cell
        event.which = 74;
        event.keyCode = 74;
        manager.command_mode();
        manager.handle_keydown(event);
    }
}

mpl.figure.prototype.handle_save = function(fig, msg) {
    fig.ondownload(fig, null);
}


mpl.find_output_cell = function(html_output) {
    // Return the cell and output element which can be found *uniquely* in the notebook.
    // Note - this is a bit hacky, but it is done because the "notebook_saving.Notebook"
    // IPython event is triggered only after the cells have been serialised, which for
    // our purposes (turning an active figure into a static one), is too late.
    var cells = IPython.notebook.get_cells();
    var ncells = cells.length;
    for (var i=0; i<ncells; i++) {
        var cell = cells[i];
        if (cell.cell_type === 'code'){
            for (var j=0; j<cell.output_area.outputs.length; j++) {
                var data = cell.output_area.outputs[j];
                if (data.data) {
                    // IPython >= 3 moved mimebundle to data attribute of output
                    data = data.data;
                }
                if (data['text/html'] == html_output) {
                    return [cell, data, j];
                }
            }
        }
    }
}

// Register the function which deals with the matplotlib target/channel.
// The kernel may be null if the page has been refreshed.
if (IPython.notebook.kernel != null) {
    IPython.notebook.kernel.comm_manager.register_target('matplotlib', mpl.mpl_figure_comm);
}

</script>
</div>

</div>

<div class="output_area"><div class="prompt"></div>

<div class="output_html rendered_html output_subarea ">
<img src="data:image/png;base64,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">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="3.-How-did-the-number-of-impressions-seen-by-each-user-influence-the-effectiveness-of-advertising?">3. How did the number of impressions seen by each user influence the effectiveness of advertising?<a class="anchor-link" href="#3.-How-did-the-number-of-impressions-seen-by-each-user-influence-the-effectiveness-of-advertising?">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>a. Create a chart of conversion rates as a function of the number of ads displayed to users. 
Plot conversion rates for those who were exposed to the ad. 
Group together number of impressions as necessary to obtain a meaningful plot.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[26]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="k">def</span> <span class="nf">PlotImpressionVsConversion</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">binwidth</span><span class="o">=</span><span class="mi">50</span><span class="p">):</span>
    <span class="n">bins</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">bins</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">cut</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">],</span> <span class="n">bins</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="nb">min</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">])</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span> \
                                                   <span class="nb">max</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">])</span><span class="o">+</span><span class="n">binwidth</span><span class="p">,</span> <span class="n">binwidth</span><span class="p">))</span>

    <span class="n">y</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="n">bins</span><span class="p">)</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span> <span class="o">/</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="n">bins</span><span class="p">)</span><span class="o">.</span><span class="n">count</span><span class="p">()</span> <span class="o">*</span> <span class="mi">100</span>
    
    <span class="k">print</span> <span class="s">&quot;Grouped impression ranges and corresponding conversion </span><span class="si">% r</span><span class="s">ates (all groups):&quot;</span>
    <span class="k">print</span> <span class="n">y</span>
    <span class="k">print</span> <span class="s">&quot;Chart of conversion rates as a function of the number of ads displayed to all users:&quot;</span>
    
    <span class="n">g1</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">y</span><span class="o">.</span><span class="n">index</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="n">y</span><span class="o">.</span><span class="n">values</span><span class="p">)</span>
    <span class="n">g1</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s">&#39;Total Impressions vs. Conversion Rates For All Groups&#39;</span><span class="p">)</span>
    <span class="n">g1</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s">&#39;Total Impressions&#39;</span><span class="p">)</span>
    <span class="n">g1</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s">&#39;Conversion Rates (%)&#39;</span><span class="p">)</span>
    <span class="n">g1</span><span class="o">.</span><span class="n">set_xticklabels</span><span class="p">(</span><span class="n">g1</span><span class="o">.</span><span class="n">get_xticklabels</span><span class="p">(),</span><span class="n">rotation</span><span class="o">=</span><span class="mi">270</span><span class="p">)</span>

<span class="n">PlotImpressionVsConversion</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">binwidth</span><span class="o">=</span><span class="mi">100</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Grouped impression ranges and corresponding conversion % rates (all groups):
tot_impr
(0, 100]          1.936864
(100, 200]       17.367929
(200, 300]       15.302391
(300, 400]       16.053250
(400, 500]       14.392523
(500, 600]       15.625000
(600, 700]       18.750000
(700, 800]       20.689655
(800, 900]       10.810811
(900, 1000]      16.000000
(1000, 1100]      7.692308
(1100, 1200]     14.285714
(1200, 1300]      0.000000
(1300, 1400]     42.857143
(1400, 1500]     50.000000
(1500, 1600]           NaN
(1600, 1700]     50.000000
(1700, 1800]    100.000000
(1800, 1900]           NaN
(1900, 2000]           NaN
(2000, 2100]      0.000000
dtype: float64
Chart of conversion rates as a function of the number of ads displayed to all users:
</pre>
</div>
</div>

<div class="output_area"><div class="prompt"></div>


<div class="output_subarea output_javascript ">
<script type="text/javascript">
/* Put everything inside the global mpl namespace */
window.mpl = {};

mpl.get_websocket_type = function() {
    if (typeof(WebSocket) !== 'undefined') {
        return WebSocket;
    } else if (typeof(MozWebSocket) !== 'undefined') {
        return MozWebSocket;
    } else {
        alert('Your browser does not have WebSocket support.' +
              'Please try Chrome, Safari or Firefox ≥ 6. ' +
              'Firefox 4 and 5 are also supported but you ' +
              'have to enable WebSockets in about:config.');
    };
}

mpl.figure = function(figure_id, websocket, ondownload, parent_element) {
    this.id = figure_id;

    this.ws = websocket;

    this.supports_binary = (this.ws.binaryType != undefined);

    if (!this.supports_binary) {
        var warnings = document.getElementById("mpl-warnings");
        if (warnings) {
            warnings.style.display = 'block';
            warnings.textContent = (
                "This browser does not support binary websocket messages. " +
                    "Performance may be slow.");
        }
    }

    this.imageObj = new Image();

    this.context = undefined;
    this.message = undefined;
    this.canvas = undefined;
    this.rubberband_canvas = undefined;
    this.rubberband_context = undefined;
    this.format_dropdown = undefined;

    this.image_mode = 'full';

    this.root = $('<div/>');
    this._root_extra_style(this.root)
    this.root.attr('style', 'display: inline-block');

    $(parent_element).append(this.root);

    this._init_header(this);
    this._init_canvas(this);
    this._init_toolbar(this);

    var fig = this;

    this.waiting = false;

    this.ws.onopen =  function () {
            fig.send_message("supports_binary", {value: fig.supports_binary});
            fig.send_message("send_image_mode", {});
            fig.send_message("refresh", {});
        }

    this.imageObj.onload = function() {
            if (fig.image_mode == 'full') {
                // Full images could contain transparency (where diff images
                // almost always do), so we need to clear the canvas so that
                // there is no ghosting.
                fig.context.clearRect(0, 0, fig.canvas.width, fig.canvas.height);
            }
            fig.context.drawImage(fig.imageObj, 0, 0);
        };

    this.imageObj.onunload = function() {
        this.ws.close();
    }

    this.ws.onmessage = this._make_on_message_function(this);

    this.ondownload = ondownload;
}

mpl.figure.prototype._init_header = function() {
    var titlebar = $(
        '<div class="ui-dialog-titlebar ui-widget-header ui-corner-all ' +
        'ui-helper-clearfix"/>');
    var titletext = $(
        '<div class="ui-dialog-title" style="width: 100%; ' +
        'text-align: center; padding: 3px;"/>');
    titlebar.append(titletext)
    this.root.append(titlebar);
    this.header = titletext[0];
}



mpl.figure.prototype._canvas_extra_style = function(canvas_div) {

}


mpl.figure.prototype._root_extra_style = function(canvas_div) {

}

mpl.figure.prototype._init_canvas = function() {
    var fig = this;

    var canvas_div = $('<div/>');

    canvas_div.attr('style', 'position: relative; clear: both; outline: 0');

    function canvas_keyboard_event(event) {
        return fig.key_event(event, event['data']);
    }

    canvas_div.keydown('key_press', canvas_keyboard_event);
    canvas_div.keyup('key_release', canvas_keyboard_event);
    this.canvas_div = canvas_div
    this._canvas_extra_style(canvas_div)
    this.root.append(canvas_div);

    var canvas = $('<canvas/>');
    canvas.addClass('mpl-canvas');
    canvas.attr('style', "left: 0; top: 0; z-index: 0; outline: 0")

    this.canvas = canvas[0];
    this.context = canvas[0].getContext("2d");

    var rubberband = $('<canvas/>');
    rubberband.attr('style', "position: absolute; left: 0; top: 0; z-index: 1;")

    var pass_mouse_events = true;

    canvas_div.resizable({
        start: function(event, ui) {
            pass_mouse_events = false;
        },
        resize: function(event, ui) {
            fig.request_resize(ui.size.width, ui.size.height);
        },
        stop: function(event, ui) {
            pass_mouse_events = true;
            fig.request_resize(ui.size.width, ui.size.height);
        },
    });

    function mouse_event_fn(event) {
        if (pass_mouse_events)
            return fig.mouse_event(event, event['data']);
    }

    rubberband.mousedown('button_press', mouse_event_fn);
    rubberband.mouseup('button_release', mouse_event_fn);
    // Throttle sequential mouse events to 1 every 20ms.
    rubberband.mousemove('motion_notify', mouse_event_fn);

    rubberband.mouseenter('figure_enter', mouse_event_fn);
    rubberband.mouseleave('figure_leave', mouse_event_fn);

    canvas_div.on("wheel", function (event) {
        event = event.originalEvent;
        event['data'] = 'scroll'
        if (event.deltaY < 0) {
            event.step = 1;
        } else {
            event.step = -1;
        }
        mouse_event_fn(event);
    });

    canvas_div.append(canvas);
    canvas_div.append(rubberband);

    this.rubberband = rubberband;
    this.rubberband_canvas = rubberband[0];
    this.rubberband_context = rubberband[0].getContext("2d");
    this.rubberband_context.strokeStyle = "#000000";

    this._resize_canvas = function(width, height) {
        // Keep the size of the canvas, canvas container, and rubber band
        // canvas in synch.
        canvas_div.css('width', width)
        canvas_div.css('height', height)

        canvas.attr('width', width);
        canvas.attr('height', height);

        rubberband.attr('width', width);
        rubberband.attr('height', height);
    }

    // Set the figure to an initial 600x600px, this will subsequently be updated
    // upon first draw.
    this._resize_canvas(600, 600);

    // Disable right mouse context menu.
    $(this.rubberband_canvas).bind("contextmenu",function(e){
        return false;
    });

    function set_focus () {
        canvas.focus();
        canvas_div.focus();
    }

    window.setTimeout(set_focus, 100);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items) {
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) {
            // put a spacer in here.
            continue;
        }
        var button = $('<button/>');
        button.addClass('ui-button ui-widget ui-state-default ui-corner-all ' +
                        'ui-button-icon-only');
        button.attr('role', 'button');
        button.attr('aria-disabled', 'false');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);

        var icon_img = $('<span/>');
        icon_img.addClass('ui-button-icon-primary ui-icon');
        icon_img.addClass(image);
        icon_img.addClass('ui-corner-all');

        var tooltip_span = $('<span/>');
        tooltip_span.addClass('ui-button-text');
        tooltip_span.html(tooltip);

        button.append(icon_img);
        button.append(tooltip_span);

        nav_element.append(button);
    }

    var fmt_picker_span = $('<span/>');

    var fmt_picker = $('<select/>');
    fmt_picker.addClass('mpl-toolbar-option ui-widget ui-widget-content');
    fmt_picker_span.append(fmt_picker);
    nav_element.append(fmt_picker_span);
    this.format_dropdown = fmt_picker[0];

    for (var ind in mpl.extensions) {
        var fmt = mpl.extensions[ind];
        var option = $(
            '<option/>', {selected: fmt === mpl.default_extension}).html(fmt);
        fmt_picker.append(option)
    }

    // Add hover states to the ui-buttons
    $( ".ui-button" ).hover(
        function() { $(this).addClass("ui-state-hover");},
        function() { $(this).removeClass("ui-state-hover");}
    );

    var status_bar = $('<span class="mpl-message"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];
}

mpl.figure.prototype.request_resize = function(x_pixels, y_pixels) {
    // Request matplotlib to resize the figure. Matplotlib will then trigger a resize in the client,
    // which will in turn request a refresh of the image.
    this.send_message('resize', {'width': x_pixels, 'height': y_pixels});
}

mpl.figure.prototype.send_message = function(type, properties) {
    properties['type'] = type;
    properties['figure_id'] = this.id;
    this.ws.send(JSON.stringify(properties));
}

mpl.figure.prototype.send_draw_message = function() {
    if (!this.waiting) {
        this.waiting = true;
        this.ws.send(JSON.stringify({type: "draw", figure_id: this.id}));
    }
}


mpl.figure.prototype.handle_save = function(fig, msg) {
    var format_dropdown = fig.format_dropdown;
    var format = format_dropdown.options[format_dropdown.selectedIndex].value;
    fig.ondownload(fig, format);
}


mpl.figure.prototype.handle_resize = function(fig, msg) {
    var size = msg['size'];
    if (size[0] != fig.canvas.width || size[1] != fig.canvas.height) {
        fig._resize_canvas(size[0], size[1]);
        fig.send_message("refresh", {});
    };
}

mpl.figure.prototype.handle_rubberband = function(fig, msg) {
    var x0 = msg['x0'];
    var y0 = fig.canvas.height - msg['y0'];
    var x1 = msg['x1'];
    var y1 = fig.canvas.height - msg['y1'];
    x0 = Math.floor(x0) + 0.5;
    y0 = Math.floor(y0) + 0.5;
    x1 = Math.floor(x1) + 0.5;
    y1 = Math.floor(y1) + 0.5;
    var min_x = Math.min(x0, x1);
    var min_y = Math.min(y0, y1);
    var width = Math.abs(x1 - x0);
    var height = Math.abs(y1 - y0);

    fig.rubberband_context.clearRect(
        0, 0, fig.canvas.width, fig.canvas.height);

    fig.rubberband_context.strokeRect(min_x, min_y, width, height);
}

mpl.figure.prototype.handle_figure_label = function(fig, msg) {
    // Updates the figure title.
    fig.header.textContent = msg['label'];
}

mpl.figure.prototype.handle_cursor = function(fig, msg) {
    var cursor = msg['cursor'];
    switch(cursor)
    {
    case 0:
        cursor = 'pointer';
        break;
    case 1:
        cursor = 'default';
        break;
    case 2:
        cursor = 'crosshair';
        break;
    case 3:
        cursor = 'move';
        break;
    }
    fig.rubberband_canvas.style.cursor = cursor;
}

mpl.figure.prototype.handle_message = function(fig, msg) {
    fig.message.textContent = msg['message'];
}

mpl.figure.prototype.handle_draw = function(fig, msg) {
    // Request the server to send over a new figure.
    fig.send_draw_message();
}

mpl.figure.prototype.handle_image_mode = function(fig, msg) {
    fig.image_mode = msg['mode'];
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Called whenever the canvas gets updated.
    this.send_message("ack", {});
}

// A function to construct a web socket function for onmessage handling.
// Called in the figure constructor.
mpl.figure.prototype._make_on_message_function = function(fig) {
    return function socket_on_message(evt) {
        if (evt.data instanceof Blob) {
            /* FIXME: We get "Resource interpreted as Image but
             * transferred with MIME type text/plain:" errors on
             * Chrome.  But how to set the MIME type?  It doesn't seem
             * to be part of the websocket stream */
            evt.data.type = "image/png";

            /* Free the memory for the previous frames */
            if (fig.imageObj.src) {
                (window.URL || window.webkitURL).revokeObjectURL(
                    fig.imageObj.src);
            }

            fig.imageObj.src = (window.URL || window.webkitURL).createObjectURL(
                evt.data);
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }
        else if (typeof evt.data === 'string' && evt.data.slice(0, 21) == "data:image/png;base64") {
            fig.imageObj.src = evt.data;
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }

        var msg = JSON.parse(evt.data);
        var msg_type = msg['type'];

        // Call the  "handle_{type}" callback, which takes
        // the figure and JSON message as its only arguments.
        try {
            var callback = fig["handle_" + msg_type];
        } catch (e) {
            console.log("No handler for the '" + msg_type + "' message type: ", msg);
            return;
        }

        if (callback) {
            try {
                // console.log("Handling '" + msg_type + "' message: ", msg);
                callback(fig, msg);
            } catch (e) {
                console.log("Exception inside the 'handler_" + msg_type + "' callback:", e, e.stack, msg);
            }
        }
    };
}

// from http://stackoverflow.com/questions/1114465/getting-mouse-location-in-canvas
mpl.findpos = function(e) {
    //this section is from http://www.quirksmode.org/js/events_properties.html
    var targ;
    if (!e)
        e = window.event;
    if (e.target)
        targ = e.target;
    else if (e.srcElement)
        targ = e.srcElement;
    if (targ.nodeType == 3) // defeat Safari bug
        targ = targ.parentNode;

    // jQuery normalizes the pageX and pageY
    // pageX,Y are the mouse positions relative to the document
    // offset() returns the position of the element relative to the document
    var x = e.pageX - $(targ).offset().left;
    var y = e.pageY - $(targ).offset().top;

    return {"x": x, "y": y};
};

/*
 * return a copy of an object with only non-object keys
 * we need this to avoid circular references
 * http://stackoverflow.com/a/24161582/3208463
 */
function simpleKeys (original) {
  return Object.keys(original).reduce(function (obj, key) {
    if (typeof original[key] !== 'object')
        obj[key] = original[key]
    return obj;
  }, {});
}

mpl.figure.prototype.mouse_event = function(event, name) {
    var canvas_pos = mpl.findpos(event)

    if (name === 'button_press')
    {
        this.canvas.focus();
        this.canvas_div.focus();
    }

    var x = canvas_pos.x;
    var y = canvas_pos.y;

    this.send_message(name, {x: x, y: y, button: event.button,
                             step: event.step,
                             guiEvent: simpleKeys(event)});

    /* This prevents the web browser from automatically changing to
     * the text insertion cursor when the button is pressed.  We want
     * to control all of the cursor setting manually through the
     * 'cursor' event from matplotlib */
    event.preventDefault();
    return false;
}

mpl.figure.prototype._key_event_extra = function(event, name) {
    // Handle any extra behaviour associated with a key event
}

mpl.figure.prototype.key_event = function(event, name) {

    // Prevent repeat events
    if (name == 'key_press')
    {
        if (event.which === this._key)
            return;
        else
            this._key = event.which;
    }
    if (name == 'key_release')
        this._key = null;

    var value = '';
    if (event.ctrlKey && event.which != 17)
        value += "ctrl+";
    if (event.altKey && event.which != 18)
        value += "alt+";
    if (event.shiftKey && event.which != 16)
        value += "shift+";

    value += 'k';
    value += event.which.toString();

    this._key_event_extra(event, name);

    this.send_message(name, {key: value,
                             guiEvent: simpleKeys(event)});
    return false;
}

mpl.figure.prototype.toolbar_button_onclick = function(name) {
    if (name == 'download') {
        this.handle_save(this, null);
    } else {
        this.send_message("toolbar_button", {name: name});
    }
};

mpl.figure.prototype.toolbar_button_onmouseover = function(tooltip) {
    this.message.textContent = tooltip;
};
mpl.toolbar_items = [["Home", "Reset original view", "fa fa-home icon-home", "home"], ["Back", "Back to  previous view", "fa fa-arrow-left icon-arrow-left", "back"], ["Forward", "Forward to next view", "fa fa-arrow-right icon-arrow-right", "forward"], ["", "", "", ""], ["Pan", "Pan axes with left mouse, zoom with right", "fa fa-arrows icon-move", "pan"], ["Zoom", "Zoom to rectangle", "fa fa-square-o icon-check-empty", "zoom"], ["", "", "", ""], ["Download", "Download plot", "fa fa-floppy-o icon-save", "download"]];

mpl.extensions = ["eps", "jpeg", "pdf", "png", "ps", "raw", "svg", "tif"];

mpl.default_extension = "png";var comm_websocket_adapter = function(comm) {
    // Create a "websocket"-like object which calls the given IPython comm
    // object with the appropriate methods. Currently this is a non binary
    // socket, so there is still some room for performance tuning.
    var ws = {};

    ws.close = function() {
        comm.close()
    };
    ws.send = function(m) {
        //console.log('sending', m);
        comm.send(m);
    };
    // Register the callback with on_msg.
    comm.on_msg(function(msg) {
        //console.log('receiving', msg['content']['data'], msg);
        // Pass the mpl event to the overriden (by mpl) onmessage function.
        ws.onmessage(msg['content']['data'])
    });
    return ws;
}

mpl.mpl_figure_comm = function(comm, msg) {
    // This is the function which gets called when the mpl process
    // starts-up an IPython Comm through the "matplotlib" channel.

    var id = msg.content.data.id;
    // Get hold of the div created by the display call when the Comm
    // socket was opened in Python.
    var element = $("#" + id);
    var ws_proxy = comm_websocket_adapter(comm)

    function ondownload(figure, format) {
        window.open(figure.imageObj.src);
    }

    var fig = new mpl.figure(id, ws_proxy,
                           ondownload,
                           element.get(0));

    // Call onopen now - mpl needs it, as it is assuming we've passed it a real
    // web socket which is closed, not our websocket->open comm proxy.
    ws_proxy.onopen();

    fig.parent_element = element.get(0);
    fig.cell_info = mpl.find_output_cell("<div id='" + id + "'></div>");
    if (!fig.cell_info) {
        console.error("Failed to find cell for figure", id, fig);
        return;
    }

    var output_index = fig.cell_info[2]
    var cell = fig.cell_info[0];

};

mpl.figure.prototype.handle_close = function(fig, msg) {
    fig.root.unbind('remove')

    // Update the output cell to use the data from the current canvas.
    fig.push_to_output();
    var dataURL = fig.canvas.toDataURL();
    // Re-enable the keyboard manager in IPython - without this line, in FF,
    // the notebook keyboard shortcuts fail.
    IPython.keyboard_manager.enable()
    $(fig.parent_element).html('<img src="' + dataURL + '">');
    fig.close_ws(fig, msg);
}

mpl.figure.prototype.close_ws = function(fig, msg){
    fig.send_message('closing', msg);
    // fig.ws.close()
}

mpl.figure.prototype.push_to_output = function(remove_interactive) {
    // Turn the data on the canvas into data in the output cell.
    var dataURL = this.canvas.toDataURL();
    this.cell_info[1]['text/html'] = '<img src="' + dataURL + '">';
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Tell IPython that the notebook contents must change.
    IPython.notebook.set_dirty(true);
    this.send_message("ack", {});
    var fig = this;
    // Wait a second, then push the new image to the DOM so
    // that it is saved nicely (might be nice to debounce this).
    setTimeout(function () { fig.push_to_output() }, 1000);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items){
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) { continue; };

        var button = $('<button class="btn btn-default" href="#" title="' + name + '"><i class="fa ' + image + ' fa-lg"></i></button>');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);
        nav_element.append(button);
    }

    // Add the status bar.
    var status_bar = $('<span class="mpl-message" style="text-align:right; float: right;"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];

    // Add the close button to the window.
    var buttongrp = $('<div class="btn-group inline pull-right"></div>');
    var button = $('<button class="btn btn-mini btn-primary" href="#" title="Stop Interaction"><i class="fa fa-power-off icon-remove icon-large"></i></button>');
    button.click(function (evt) { fig.handle_close(fig, {}); } );
    button.mouseover('Stop Interaction', toolbar_mouse_event);
    buttongrp.append(button);
    var titlebar = this.root.find($('.ui-dialog-titlebar'));
    titlebar.prepend(buttongrp);
}

mpl.figure.prototype._root_extra_style = function(el){
    var fig = this
    el.on("remove", function(){
	fig.close_ws(fig, {});
    });
}

mpl.figure.prototype._canvas_extra_style = function(el){
    // this is important to make the div 'focusable
    el.attr('tabindex', 0)
    // reach out to IPython and tell the keyboard manager to turn it's self
    // off when our div gets focus

    // location in version 3
    if (IPython.notebook.keyboard_manager) {
        IPython.notebook.keyboard_manager.register_events(el);
    }
    else {
        // location in version 2
        IPython.keyboard_manager.register_events(el);
    }

}

mpl.figure.prototype._key_event_extra = function(event, name) {
    var manager = IPython.notebook.keyboard_manager;
    if (!manager)
        manager = IPython.keyboard_manager;

    // Check for shift+enter
    if (event.shiftKey && event.which == 13) {
        this.canvas_div.blur();
        event.shiftKey = false;
        // Send a "J" for go to next cell
        event.which = 74;
        event.keyCode = 74;
        manager.command_mode();
        manager.handle_keydown(event);
    }
}

mpl.figure.prototype.handle_save = function(fig, msg) {
    fig.ondownload(fig, null);
}


mpl.find_output_cell = function(html_output) {
    // Return the cell and output element which can be found *uniquely* in the notebook.
    // Note - this is a bit hacky, but it is done because the "notebook_saving.Notebook"
    // IPython event is triggered only after the cells have been serialised, which for
    // our purposes (turning an active figure into a static one), is too late.
    var cells = IPython.notebook.get_cells();
    var ncells = cells.length;
    for (var i=0; i<ncells; i++) {
        var cell = cells[i];
        if (cell.cell_type === 'code'){
            for (var j=0; j<cell.output_area.outputs.length; j++) {
                var data = cell.output_area.outputs[j];
                if (data.data) {
                    // IPython >= 3 moved mimebundle to data attribute of output
                    data = data.data;
                }
                if (data['text/html'] == html_output) {
                    return [cell, data, j];
                }
            }
        }
    }
}

// Register the function which deals with the matplotlib target/channel.
// The kernel may be null if the page has been refreshed.
if (IPython.notebook.kernel != null) {
    IPython.notebook.kernel.comm_manager.register_target('matplotlib', mpl.mpl_figure_comm);
}

</script>
</div>

</div>

<div class="output_area"><div class="prompt"></div>

<div class="output_html rendered_html output_subarea ">
<img src="data:image/png;base64,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">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[27]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="k">def</span> <span class="nf">PlotImpressionVsConversionTest</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">binwidth</span><span class="o">=</span><span class="mi">50</span><span class="p">):</span>
    <span class="n">bins</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">bins</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">cut</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">],</span> <span class="n">bins</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="nb">min</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">])</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span> \
                                                                  <span class="nb">max</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">])</span><span class="o">+</span><span class="n">binwidth</span><span class="p">,</span> <span class="n">binwidth</span><span class="p">))</span>

    <span class="n">y</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="n">bins</span><span class="p">)</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span> <span class="o">/</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="n">bins</span><span class="p">)</span><span class="o">.</span><span class="n">count</span><span class="p">()</span> <span class="o">*</span> <span class="mi">100</span>
    
    <span class="k">print</span> <span class="s">&quot;Grouped impression ranges and corresponding conversion </span><span class="si">% r</span><span class="s">ates (test group):&quot;</span>
    <span class="k">print</span> <span class="n">y</span>
    <span class="k">print</span> <span class="s">&quot;Chart of conversion rates as a function of the number of ads displayed to test group users:&quot;</span>
    
    <span class="n">g2</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">y</span><span class="o">.</span><span class="n">index</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="n">y</span><span class="o">.</span><span class="n">values</span><span class="p">)</span>
    <span class="n">g2</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s">&#39;Total Impressions vs. Conversion Rates For Test Group Users&#39;</span><span class="p">)</span>
    <span class="n">g2</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s">&#39;Total Impressions&#39;</span><span class="p">)</span>
    <span class="n">g2</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s">&#39;Conversion Rates (%)&#39;</span><span class="p">)</span>
    <span class="n">g2</span><span class="o">.</span><span class="n">set_xticklabels</span><span class="p">(</span><span class="n">g2</span><span class="o">.</span><span class="n">get_xticklabels</span><span class="p">(),</span><span class="n">rotation</span><span class="o">=</span><span class="mi">270</span><span class="p">)</span>

<span class="n">PlotImpressionVsConversionTest</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">binwidth</span><span class="o">=</span><span class="mi">100</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Grouped impression ranges and corresponding conversion % rates (test group):
tot_impr
(0, 100]          1.961944
(100, 200]       17.677262
(200, 300]       15.196223
(300, 400]       16.273393
(400, 500]       14.313725
(500, 600]       15.637860
(600, 700]       19.014085
(700, 800]       21.176471
(800, 900]       11.111111
(900, 1000]      16.666667
(1000, 1100]      7.692308
(1100, 1200]     14.285714
(1200, 1300]      0.000000
(1300, 1400]     42.857143
(1400, 1500]     50.000000
(1500, 1600]           NaN
(1600, 1700]     50.000000
(1700, 1800]    100.000000
(1800, 1900]           NaN
(1900, 2000]           NaN
(2000, 2100]      0.000000
dtype: float64
Chart of conversion rates as a function of the number of ads displayed to test group users:
</pre>
</div>
</div>

<div class="output_area"><div class="prompt"></div>


<div class="output_subarea output_javascript ">
<script type="text/javascript">
/* Put everything inside the global mpl namespace */
window.mpl = {};

mpl.get_websocket_type = function() {
    if (typeof(WebSocket) !== 'undefined') {
        return WebSocket;
    } else if (typeof(MozWebSocket) !== 'undefined') {
        return MozWebSocket;
    } else {
        alert('Your browser does not have WebSocket support.' +
              'Please try Chrome, Safari or Firefox ≥ 6. ' +
              'Firefox 4 and 5 are also supported but you ' +
              'have to enable WebSockets in about:config.');
    };
}

mpl.figure = function(figure_id, websocket, ondownload, parent_element) {
    this.id = figure_id;

    this.ws = websocket;

    this.supports_binary = (this.ws.binaryType != undefined);

    if (!this.supports_binary) {
        var warnings = document.getElementById("mpl-warnings");
        if (warnings) {
            warnings.style.display = 'block';
            warnings.textContent = (
                "This browser does not support binary websocket messages. " +
                    "Performance may be slow.");
        }
    }

    this.imageObj = new Image();

    this.context = undefined;
    this.message = undefined;
    this.canvas = undefined;
    this.rubberband_canvas = undefined;
    this.rubberband_context = undefined;
    this.format_dropdown = undefined;

    this.image_mode = 'full';

    this.root = $('<div/>');
    this._root_extra_style(this.root)
    this.root.attr('style', 'display: inline-block');

    $(parent_element).append(this.root);

    this._init_header(this);
    this._init_canvas(this);
    this._init_toolbar(this);

    var fig = this;

    this.waiting = false;

    this.ws.onopen =  function () {
            fig.send_message("supports_binary", {value: fig.supports_binary});
            fig.send_message("send_image_mode", {});
            fig.send_message("refresh", {});
        }

    this.imageObj.onload = function() {
            if (fig.image_mode == 'full') {
                // Full images could contain transparency (where diff images
                // almost always do), so we need to clear the canvas so that
                // there is no ghosting.
                fig.context.clearRect(0, 0, fig.canvas.width, fig.canvas.height);
            }
            fig.context.drawImage(fig.imageObj, 0, 0);
        };

    this.imageObj.onunload = function() {
        this.ws.close();
    }

    this.ws.onmessage = this._make_on_message_function(this);

    this.ondownload = ondownload;
}

mpl.figure.prototype._init_header = function() {
    var titlebar = $(
        '<div class="ui-dialog-titlebar ui-widget-header ui-corner-all ' +
        'ui-helper-clearfix"/>');
    var titletext = $(
        '<div class="ui-dialog-title" style="width: 100%; ' +
        'text-align: center; padding: 3px;"/>');
    titlebar.append(titletext)
    this.root.append(titlebar);
    this.header = titletext[0];
}



mpl.figure.prototype._canvas_extra_style = function(canvas_div) {

}


mpl.figure.prototype._root_extra_style = function(canvas_div) {

}

mpl.figure.prototype._init_canvas = function() {
    var fig = this;

    var canvas_div = $('<div/>');

    canvas_div.attr('style', 'position: relative; clear: both; outline: 0');

    function canvas_keyboard_event(event) {
        return fig.key_event(event, event['data']);
    }

    canvas_div.keydown('key_press', canvas_keyboard_event);
    canvas_div.keyup('key_release', canvas_keyboard_event);
    this.canvas_div = canvas_div
    this._canvas_extra_style(canvas_div)
    this.root.append(canvas_div);

    var canvas = $('<canvas/>');
    canvas.addClass('mpl-canvas');
    canvas.attr('style', "left: 0; top: 0; z-index: 0; outline: 0")

    this.canvas = canvas[0];
    this.context = canvas[0].getContext("2d");

    var rubberband = $('<canvas/>');
    rubberband.attr('style', "position: absolute; left: 0; top: 0; z-index: 1;")

    var pass_mouse_events = true;

    canvas_div.resizable({
        start: function(event, ui) {
            pass_mouse_events = false;
        },
        resize: function(event, ui) {
            fig.request_resize(ui.size.width, ui.size.height);
        },
        stop: function(event, ui) {
            pass_mouse_events = true;
            fig.request_resize(ui.size.width, ui.size.height);
        },
    });

    function mouse_event_fn(event) {
        if (pass_mouse_events)
            return fig.mouse_event(event, event['data']);
    }

    rubberband.mousedown('button_press', mouse_event_fn);
    rubberband.mouseup('button_release', mouse_event_fn);
    // Throttle sequential mouse events to 1 every 20ms.
    rubberband.mousemove('motion_notify', mouse_event_fn);

    rubberband.mouseenter('figure_enter', mouse_event_fn);
    rubberband.mouseleave('figure_leave', mouse_event_fn);

    canvas_div.on("wheel", function (event) {
        event = event.originalEvent;
        event['data'] = 'scroll'
        if (event.deltaY < 0) {
            event.step = 1;
        } else {
            event.step = -1;
        }
        mouse_event_fn(event);
    });

    canvas_div.append(canvas);
    canvas_div.append(rubberband);

    this.rubberband = rubberband;
    this.rubberband_canvas = rubberband[0];
    this.rubberband_context = rubberband[0].getContext("2d");
    this.rubberband_context.strokeStyle = "#000000";

    this._resize_canvas = function(width, height) {
        // Keep the size of the canvas, canvas container, and rubber band
        // canvas in synch.
        canvas_div.css('width', width)
        canvas_div.css('height', height)

        canvas.attr('width', width);
        canvas.attr('height', height);

        rubberband.attr('width', width);
        rubberband.attr('height', height);
    }

    // Set the figure to an initial 600x600px, this will subsequently be updated
    // upon first draw.
    this._resize_canvas(600, 600);

    // Disable right mouse context menu.
    $(this.rubberband_canvas).bind("contextmenu",function(e){
        return false;
    });

    function set_focus () {
        canvas.focus();
        canvas_div.focus();
    }

    window.setTimeout(set_focus, 100);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items) {
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) {
            // put a spacer in here.
            continue;
        }
        var button = $('<button/>');
        button.addClass('ui-button ui-widget ui-state-default ui-corner-all ' +
                        'ui-button-icon-only');
        button.attr('role', 'button');
        button.attr('aria-disabled', 'false');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);

        var icon_img = $('<span/>');
        icon_img.addClass('ui-button-icon-primary ui-icon');
        icon_img.addClass(image);
        icon_img.addClass('ui-corner-all');

        var tooltip_span = $('<span/>');
        tooltip_span.addClass('ui-button-text');
        tooltip_span.html(tooltip);

        button.append(icon_img);
        button.append(tooltip_span);

        nav_element.append(button);
    }

    var fmt_picker_span = $('<span/>');

    var fmt_picker = $('<select/>');
    fmt_picker.addClass('mpl-toolbar-option ui-widget ui-widget-content');
    fmt_picker_span.append(fmt_picker);
    nav_element.append(fmt_picker_span);
    this.format_dropdown = fmt_picker[0];

    for (var ind in mpl.extensions) {
        var fmt = mpl.extensions[ind];
        var option = $(
            '<option/>', {selected: fmt === mpl.default_extension}).html(fmt);
        fmt_picker.append(option)
    }

    // Add hover states to the ui-buttons
    $( ".ui-button" ).hover(
        function() { $(this).addClass("ui-state-hover");},
        function() { $(this).removeClass("ui-state-hover");}
    );

    var status_bar = $('<span class="mpl-message"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];
}

mpl.figure.prototype.request_resize = function(x_pixels, y_pixels) {
    // Request matplotlib to resize the figure. Matplotlib will then trigger a resize in the client,
    // which will in turn request a refresh of the image.
    this.send_message('resize', {'width': x_pixels, 'height': y_pixels});
}

mpl.figure.prototype.send_message = function(type, properties) {
    properties['type'] = type;
    properties['figure_id'] = this.id;
    this.ws.send(JSON.stringify(properties));
}

mpl.figure.prototype.send_draw_message = function() {
    if (!this.waiting) {
        this.waiting = true;
        this.ws.send(JSON.stringify({type: "draw", figure_id: this.id}));
    }
}


mpl.figure.prototype.handle_save = function(fig, msg) {
    var format_dropdown = fig.format_dropdown;
    var format = format_dropdown.options[format_dropdown.selectedIndex].value;
    fig.ondownload(fig, format);
}


mpl.figure.prototype.handle_resize = function(fig, msg) {
    var size = msg['size'];
    if (size[0] != fig.canvas.width || size[1] != fig.canvas.height) {
        fig._resize_canvas(size[0], size[1]);
        fig.send_message("refresh", {});
    };
}

mpl.figure.prototype.handle_rubberband = function(fig, msg) {
    var x0 = msg['x0'];
    var y0 = fig.canvas.height - msg['y0'];
    var x1 = msg['x1'];
    var y1 = fig.canvas.height - msg['y1'];
    x0 = Math.floor(x0) + 0.5;
    y0 = Math.floor(y0) + 0.5;
    x1 = Math.floor(x1) + 0.5;
    y1 = Math.floor(y1) + 0.5;
    var min_x = Math.min(x0, x1);
    var min_y = Math.min(y0, y1);
    var width = Math.abs(x1 - x0);
    var height = Math.abs(y1 - y0);

    fig.rubberband_context.clearRect(
        0, 0, fig.canvas.width, fig.canvas.height);

    fig.rubberband_context.strokeRect(min_x, min_y, width, height);
}

mpl.figure.prototype.handle_figure_label = function(fig, msg) {
    // Updates the figure title.
    fig.header.textContent = msg['label'];
}

mpl.figure.prototype.handle_cursor = function(fig, msg) {
    var cursor = msg['cursor'];
    switch(cursor)
    {
    case 0:
        cursor = 'pointer';
        break;
    case 1:
        cursor = 'default';
        break;
    case 2:
        cursor = 'crosshair';
        break;
    case 3:
        cursor = 'move';
        break;
    }
    fig.rubberband_canvas.style.cursor = cursor;
}

mpl.figure.prototype.handle_message = function(fig, msg) {
    fig.message.textContent = msg['message'];
}

mpl.figure.prototype.handle_draw = function(fig, msg) {
    // Request the server to send over a new figure.
    fig.send_draw_message();
}

mpl.figure.prototype.handle_image_mode = function(fig, msg) {
    fig.image_mode = msg['mode'];
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Called whenever the canvas gets updated.
    this.send_message("ack", {});
}

// A function to construct a web socket function for onmessage handling.
// Called in the figure constructor.
mpl.figure.prototype._make_on_message_function = function(fig) {
    return function socket_on_message(evt) {
        if (evt.data instanceof Blob) {
            /* FIXME: We get "Resource interpreted as Image but
             * transferred with MIME type text/plain:" errors on
             * Chrome.  But how to set the MIME type?  It doesn't seem
             * to be part of the websocket stream */
            evt.data.type = "image/png";

            /* Free the memory for the previous frames */
            if (fig.imageObj.src) {
                (window.URL || window.webkitURL).revokeObjectURL(
                    fig.imageObj.src);
            }

            fig.imageObj.src = (window.URL || window.webkitURL).createObjectURL(
                evt.data);
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }
        else if (typeof evt.data === 'string' && evt.data.slice(0, 21) == "data:image/png;base64") {
            fig.imageObj.src = evt.data;
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }

        var msg = JSON.parse(evt.data);
        var msg_type = msg['type'];

        // Call the  "handle_{type}" callback, which takes
        // the figure and JSON message as its only arguments.
        try {
            var callback = fig["handle_" + msg_type];
        } catch (e) {
            console.log("No handler for the '" + msg_type + "' message type: ", msg);
            return;
        }

        if (callback) {
            try {
                // console.log("Handling '" + msg_type + "' message: ", msg);
                callback(fig, msg);
            } catch (e) {
                console.log("Exception inside the 'handler_" + msg_type + "' callback:", e, e.stack, msg);
            }
        }
    };
}

// from http://stackoverflow.com/questions/1114465/getting-mouse-location-in-canvas
mpl.findpos = function(e) {
    //this section is from http://www.quirksmode.org/js/events_properties.html
    var targ;
    if (!e)
        e = window.event;
    if (e.target)
        targ = e.target;
    else if (e.srcElement)
        targ = e.srcElement;
    if (targ.nodeType == 3) // defeat Safari bug
        targ = targ.parentNode;

    // jQuery normalizes the pageX and pageY
    // pageX,Y are the mouse positions relative to the document
    // offset() returns the position of the element relative to the document
    var x = e.pageX - $(targ).offset().left;
    var y = e.pageY - $(targ).offset().top;

    return {"x": x, "y": y};
};

/*
 * return a copy of an object with only non-object keys
 * we need this to avoid circular references
 * http://stackoverflow.com/a/24161582/3208463
 */
function simpleKeys (original) {
  return Object.keys(original).reduce(function (obj, key) {
    if (typeof original[key] !== 'object')
        obj[key] = original[key]
    return obj;
  }, {});
}

mpl.figure.prototype.mouse_event = function(event, name) {
    var canvas_pos = mpl.findpos(event)

    if (name === 'button_press')
    {
        this.canvas.focus();
        this.canvas_div.focus();
    }

    var x = canvas_pos.x;
    var y = canvas_pos.y;

    this.send_message(name, {x: x, y: y, button: event.button,
                             step: event.step,
                             guiEvent: simpleKeys(event)});

    /* This prevents the web browser from automatically changing to
     * the text insertion cursor when the button is pressed.  We want
     * to control all of the cursor setting manually through the
     * 'cursor' event from matplotlib */
    event.preventDefault();
    return false;
}

mpl.figure.prototype._key_event_extra = function(event, name) {
    // Handle any extra behaviour associated with a key event
}

mpl.figure.prototype.key_event = function(event, name) {

    // Prevent repeat events
    if (name == 'key_press')
    {
        if (event.which === this._key)
            return;
        else
            this._key = event.which;
    }
    if (name == 'key_release')
        this._key = null;

    var value = '';
    if (event.ctrlKey && event.which != 17)
        value += "ctrl+";
    if (event.altKey && event.which != 18)
        value += "alt+";
    if (event.shiftKey && event.which != 16)
        value += "shift+";

    value += 'k';
    value += event.which.toString();

    this._key_event_extra(event, name);

    this.send_message(name, {key: value,
                             guiEvent: simpleKeys(event)});
    return false;
}

mpl.figure.prototype.toolbar_button_onclick = function(name) {
    if (name == 'download') {
        this.handle_save(this, null);
    } else {
        this.send_message("toolbar_button", {name: name});
    }
};

mpl.figure.prototype.toolbar_button_onmouseover = function(tooltip) {
    this.message.textContent = tooltip;
};
mpl.toolbar_items = [["Home", "Reset original view", "fa fa-home icon-home", "home"], ["Back", "Back to  previous view", "fa fa-arrow-left icon-arrow-left", "back"], ["Forward", "Forward to next view", "fa fa-arrow-right icon-arrow-right", "forward"], ["", "", "", ""], ["Pan", "Pan axes with left mouse, zoom with right", "fa fa-arrows icon-move", "pan"], ["Zoom", "Zoom to rectangle", "fa fa-square-o icon-check-empty", "zoom"], ["", "", "", ""], ["Download", "Download plot", "fa fa-floppy-o icon-save", "download"]];

mpl.extensions = ["eps", "jpeg", "pdf", "png", "ps", "raw", "svg", "tif"];

mpl.default_extension = "png";var comm_websocket_adapter = function(comm) {
    // Create a "websocket"-like object which calls the given IPython comm
    // object with the appropriate methods. Currently this is a non binary
    // socket, so there is still some room for performance tuning.
    var ws = {};

    ws.close = function() {
        comm.close()
    };
    ws.send = function(m) {
        //console.log('sending', m);
        comm.send(m);
    };
    // Register the callback with on_msg.
    comm.on_msg(function(msg) {
        //console.log('receiving', msg['content']['data'], msg);
        // Pass the mpl event to the overriden (by mpl) onmessage function.
        ws.onmessage(msg['content']['data'])
    });
    return ws;
}

mpl.mpl_figure_comm = function(comm, msg) {
    // This is the function which gets called when the mpl process
    // starts-up an IPython Comm through the "matplotlib" channel.

    var id = msg.content.data.id;
    // Get hold of the div created by the display call when the Comm
    // socket was opened in Python.
    var element = $("#" + id);
    var ws_proxy = comm_websocket_adapter(comm)

    function ondownload(figure, format) {
        window.open(figure.imageObj.src);
    }

    var fig = new mpl.figure(id, ws_proxy,
                           ondownload,
                           element.get(0));

    // Call onopen now - mpl needs it, as it is assuming we've passed it a real
    // web socket which is closed, not our websocket->open comm proxy.
    ws_proxy.onopen();

    fig.parent_element = element.get(0);
    fig.cell_info = mpl.find_output_cell("<div id='" + id + "'></div>");
    if (!fig.cell_info) {
        console.error("Failed to find cell for figure", id, fig);
        return;
    }

    var output_index = fig.cell_info[2]
    var cell = fig.cell_info[0];

};

mpl.figure.prototype.handle_close = function(fig, msg) {
    fig.root.unbind('remove')

    // Update the output cell to use the data from the current canvas.
    fig.push_to_output();
    var dataURL = fig.canvas.toDataURL();
    // Re-enable the keyboard manager in IPython - without this line, in FF,
    // the notebook keyboard shortcuts fail.
    IPython.keyboard_manager.enable()
    $(fig.parent_element).html('<img src="' + dataURL + '">');
    fig.close_ws(fig, msg);
}

mpl.figure.prototype.close_ws = function(fig, msg){
    fig.send_message('closing', msg);
    // fig.ws.close()
}

mpl.figure.prototype.push_to_output = function(remove_interactive) {
    // Turn the data on the canvas into data in the output cell.
    var dataURL = this.canvas.toDataURL();
    this.cell_info[1]['text/html'] = '<img src="' + dataURL + '">';
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Tell IPython that the notebook contents must change.
    IPython.notebook.set_dirty(true);
    this.send_message("ack", {});
    var fig = this;
    // Wait a second, then push the new image to the DOM so
    // that it is saved nicely (might be nice to debounce this).
    setTimeout(function () { fig.push_to_output() }, 1000);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items){
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) { continue; };

        var button = $('<button class="btn btn-default" href="#" title="' + name + '"><i class="fa ' + image + ' fa-lg"></i></button>');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);
        nav_element.append(button);
    }

    // Add the status bar.
    var status_bar = $('<span class="mpl-message" style="text-align:right; float: right;"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];

    // Add the close button to the window.
    var buttongrp = $('<div class="btn-group inline pull-right"></div>');
    var button = $('<button class="btn btn-mini btn-primary" href="#" title="Stop Interaction"><i class="fa fa-power-off icon-remove icon-large"></i></button>');
    button.click(function (evt) { fig.handle_close(fig, {}); } );
    button.mouseover('Stop Interaction', toolbar_mouse_event);
    buttongrp.append(button);
    var titlebar = this.root.find($('.ui-dialog-titlebar'));
    titlebar.prepend(buttongrp);
}

mpl.figure.prototype._root_extra_style = function(el){
    var fig = this
    el.on("remove", function(){
	fig.close_ws(fig, {});
    });
}

mpl.figure.prototype._canvas_extra_style = function(el){
    // this is important to make the div 'focusable
    el.attr('tabindex', 0)
    // reach out to IPython and tell the keyboard manager to turn it's self
    // off when our div gets focus

    // location in version 3
    if (IPython.notebook.keyboard_manager) {
        IPython.notebook.keyboard_manager.register_events(el);
    }
    else {
        // location in version 2
        IPython.keyboard_manager.register_events(el);
    }

}

mpl.figure.prototype._key_event_extra = function(event, name) {
    var manager = IPython.notebook.keyboard_manager;
    if (!manager)
        manager = IPython.keyboard_manager;

    // Check for shift+enter
    if (event.shiftKey && event.which == 13) {
        this.canvas_div.blur();
        event.shiftKey = false;
        // Send a "J" for go to next cell
        event.which = 74;
        event.keyCode = 74;
        manager.command_mode();
        manager.handle_keydown(event);
    }
}

mpl.figure.prototype.handle_save = function(fig, msg) {
    fig.ondownload(fig, null);
}


mpl.find_output_cell = function(html_output) {
    // Return the cell and output element which can be found *uniquely* in the notebook.
    // Note - this is a bit hacky, but it is done because the "notebook_saving.Notebook"
    // IPython event is triggered only after the cells have been serialised, which for
    // our purposes (turning an active figure into a static one), is too late.
    var cells = IPython.notebook.get_cells();
    var ncells = cells.length;
    for (var i=0; i<ncells; i++) {
        var cell = cells[i];
        if (cell.cell_type === 'code'){
            for (var j=0; j<cell.output_area.outputs.length; j++) {
                var data = cell.output_area.outputs[j];
                if (data.data) {
                    // IPython >= 3 moved mimebundle to data attribute of output
                    data = data.data;
                }
                if (data['text/html'] == html_output) {
                    return [cell, data, j];
                }
            }
        }
    }
}

// Register the function which deals with the matplotlib target/channel.
// The kernel may be null if the page has been refreshed.
if (IPython.notebook.kernel != null) {
    IPython.notebook.kernel.comm_manager.register_target('matplotlib', mpl.mpl_figure_comm);
}

</script>
</div>

</div>

<div class="output_area"><div class="prompt"></div>

<div class="output_html rendered_html output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAoAAAAG4CAYAAADVDFZ+AAAgAElEQVR4XuydeZwcVbm/31PVMwkhE4SQQBZCkuk61ZMICEEFVEAEroro9arggpfrxiYgOwpcNgXFDVwuiqi4oCDiCqgX+EEERFQCQkgydaqzEIZsLGImDEmmq87v8+b2xM5sXdPVfaq6+jv/aOiq9z3ned/qfvrU0oLwBwIgAAIgAAIgAAIg0FIEREvNFpMFARAAARAAARAAARAgCCCaAARAAARAAARAAARajAAEsMUKjumCAAiAAAiAAAiAAAQQPQACIAACIAACIAACLUYAAthiBcd0QQAEQAAEQAAEQAACiB4AARAAARAAARAAgRYjAAFssYJjuiAAAiAAAiAAAiAAAUQPgAAIgAAIgAAIgECLEYAAtljBMV0QAAEQAAEQAAEQgACiB0AABEAABEAABECgxQhAAFus4JguCIAACIAACIAACEAA0QMgAAIgAAIgAAIg0GIEIIAtVnBMFwRAAARAAARAAAQggOgBEAABEAABEAABEGgxAhDAFis4pgsCIAACIAACIAACEED0AAiAAAiAAAiAAAi0GAEIYIsVHNMFARAAARAAARAAAQggegAEQAAEQAAEQAAEWowABLDFCo7pggAIgAAIgAAIgAAEED0AAiAAAiAAAiAAAi1GAALYYgXHdEEABEAABEAABEAAAogeAAEQAAEQAAEQAIEWIwABbLGCY7ogAAIgAAIgAAIgAAFED4AACIAACIAACIBAixGAALZYwTFdEAABEAABEAABEIAAogdAAARAAARAAARAoMUIQABbrOCYLgiAAAiAAAiAAAhAANEDiRFwXXe653nriShIbBBIDAJNQsB13Tme561skuE2fJjg0XDESJBxAhDAjBe4UdNzXfdbWusTiEgTUTsR5Yioj4i4p7RSatJoubu6uqYFQeCHYTi9WCxuHG3bfD7faVkWb/uqYba1pZT9QojXeJ73ZKPm26i4Usobieh5pdRnGpXDVFzXdd+ntT6diPYpS/2jWuvLfd//i6kxxMkjpfxPIjpJKfXGOHEG7+s4zs1CiPcR0ZaK10pE9IhlWad1d3evqpZPSvnvQoj/9jxvQbVtx/L6CGMjrfXDvu+/dSyxhpn3JUKIC8vvEW3l94mXB94jcrmcXLp06bpacjiO83ohxK+UUtNH2l9K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lRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIgkAgBCKB57BBA88wzlRECmKlyYjIgAAIg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">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[28]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="k">def</span> <span class="nf">PlotImpressionVsConversionControl</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">binwidth</span><span class="o">=</span><span class="mi">50</span><span class="p">):</span>
    <span class="n">bins</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">bins</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">cut</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">],</span> <span class="n">bins</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="nb">min</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">])</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span> \
                                                                  <span class="nb">max</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;tot_impr&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">])</span><span class="o">+</span><span class="n">binwidth</span><span class="p">,</span> <span class="n">binwidth</span><span class="p">))</span>

    <span class="n">y</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="n">bins</span><span class="p">)</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span> <span class="o">/</span> <span class="n">df</span><span class="p">[</span><span class="s">&quot;converted&quot;</span><span class="p">][</span><span class="n">df</span><span class="p">[</span><span class="s">&quot;test&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="n">bins</span><span class="p">)</span><span class="o">.</span><span class="n">count</span><span class="p">()</span> <span class="o">*</span> <span class="mi">100</span>
    
    <span class="k">print</span> <span class="s">&quot;Grouped impression ranges and corresponding conversion </span><span class="si">% r</span><span class="s">ates (control group):&quot;</span>
    <span class="k">print</span> <span class="n">y</span>
    <span class="k">print</span> <span class="s">&quot;Chart of conversion rates as a function of the number of ads displayed to control group users:&quot;</span>
    
    <span class="n">g2</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="n">y</span><span class="o">.</span><span class="n">index</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="n">y</span><span class="o">.</span><span class="n">values</span><span class="p">)</span>
    <span class="n">g2</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s">&#39;Total Impressions vs. Conversion Rates For Control Group Users&#39;</span><span class="p">)</span>
    <span class="n">g2</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s">&#39;Total Impressions&#39;</span><span class="p">)</span>
    <span class="n">g2</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s">&#39;Conversion Rates (%)&#39;</span><span class="p">)</span>
    <span class="n">g2</span><span class="o">.</span><span class="n">set_xticklabels</span><span class="p">(</span><span class="n">g2</span><span class="o">.</span><span class="n">get_xticklabels</span><span class="p">(),</span><span class="n">rotation</span><span class="o">=</span><span class="mi">270</span><span class="p">)</span>

<span class="n">PlotImpressionVsConversionControl</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">binwidth</span><span class="o">=</span><span class="mi">100</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>Grouped impression ranges and corresponding conversion % rates (control group):
tot_impr
(0, 100]        1.332504
(100, 200]     10.638298
(200, 300]     17.469880
(300, 400]     10.416667
(400, 500]     16.000000
(500, 600]     15.384615
(600, 700]      0.000000
(700, 800]      0.000000
(800, 900]      0.000000
(900, 1000]     0.000000
dtype: float64
Chart of conversion rates as a function of the number of ads displayed to control group users:
</pre>
</div>
</div>

<div class="output_area"><div class="prompt"></div>


<div class="output_subarea output_javascript ">
<script type="text/javascript">
/* Put everything inside the global mpl namespace */
window.mpl = {};

mpl.get_websocket_type = function() {
    if (typeof(WebSocket) !== 'undefined') {
        return WebSocket;
    } else if (typeof(MozWebSocket) !== 'undefined') {
        return MozWebSocket;
    } else {
        alert('Your browser does not have WebSocket support.' +
              'Please try Chrome, Safari or Firefox ≥ 6. ' +
              'Firefox 4 and 5 are also supported but you ' +
              'have to enable WebSockets in about:config.');
    };
}

mpl.figure = function(figure_id, websocket, ondownload, parent_element) {
    this.id = figure_id;

    this.ws = websocket;

    this.supports_binary = (this.ws.binaryType != undefined);

    if (!this.supports_binary) {
        var warnings = document.getElementById("mpl-warnings");
        if (warnings) {
            warnings.style.display = 'block';
            warnings.textContent = (
                "This browser does not support binary websocket messages. " +
                    "Performance may be slow.");
        }
    }

    this.imageObj = new Image();

    this.context = undefined;
    this.message = undefined;
    this.canvas = undefined;
    this.rubberband_canvas = undefined;
    this.rubberband_context = undefined;
    this.format_dropdown = undefined;

    this.image_mode = 'full';

    this.root = $('<div/>');
    this._root_extra_style(this.root)
    this.root.attr('style', 'display: inline-block');

    $(parent_element).append(this.root);

    this._init_header(this);
    this._init_canvas(this);
    this._init_toolbar(this);

    var fig = this;

    this.waiting = false;

    this.ws.onopen =  function () {
            fig.send_message("supports_binary", {value: fig.supports_binary});
            fig.send_message("send_image_mode", {});
            fig.send_message("refresh", {});
        }

    this.imageObj.onload = function() {
            if (fig.image_mode == 'full') {
                // Full images could contain transparency (where diff images
                // almost always do), so we need to clear the canvas so that
                // there is no ghosting.
                fig.context.clearRect(0, 0, fig.canvas.width, fig.canvas.height);
            }
            fig.context.drawImage(fig.imageObj, 0, 0);
        };

    this.imageObj.onunload = function() {
        this.ws.close();
    }

    this.ws.onmessage = this._make_on_message_function(this);

    this.ondownload = ondownload;
}

mpl.figure.prototype._init_header = function() {
    var titlebar = $(
        '<div class="ui-dialog-titlebar ui-widget-header ui-corner-all ' +
        'ui-helper-clearfix"/>');
    var titletext = $(
        '<div class="ui-dialog-title" style="width: 100%; ' +
        'text-align: center; padding: 3px;"/>');
    titlebar.append(titletext)
    this.root.append(titlebar);
    this.header = titletext[0];
}



mpl.figure.prototype._canvas_extra_style = function(canvas_div) {

}


mpl.figure.prototype._root_extra_style = function(canvas_div) {

}

mpl.figure.prototype._init_canvas = function() {
    var fig = this;

    var canvas_div = $('<div/>');

    canvas_div.attr('style', 'position: relative; clear: both; outline: 0');

    function canvas_keyboard_event(event) {
        return fig.key_event(event, event['data']);
    }

    canvas_div.keydown('key_press', canvas_keyboard_event);
    canvas_div.keyup('key_release', canvas_keyboard_event);
    this.canvas_div = canvas_div
    this._canvas_extra_style(canvas_div)
    this.root.append(canvas_div);

    var canvas = $('<canvas/>');
    canvas.addClass('mpl-canvas');
    canvas.attr('style', "left: 0; top: 0; z-index: 0; outline: 0")

    this.canvas = canvas[0];
    this.context = canvas[0].getContext("2d");

    var rubberband = $('<canvas/>');
    rubberband.attr('style', "position: absolute; left: 0; top: 0; z-index: 1;")

    var pass_mouse_events = true;

    canvas_div.resizable({
        start: function(event, ui) {
            pass_mouse_events = false;
        },
        resize: function(event, ui) {
            fig.request_resize(ui.size.width, ui.size.height);
        },
        stop: function(event, ui) {
            pass_mouse_events = true;
            fig.request_resize(ui.size.width, ui.size.height);
        },
    });

    function mouse_event_fn(event) {
        if (pass_mouse_events)
            return fig.mouse_event(event, event['data']);
    }

    rubberband.mousedown('button_press', mouse_event_fn);
    rubberband.mouseup('button_release', mouse_event_fn);
    // Throttle sequential mouse events to 1 every 20ms.
    rubberband.mousemove('motion_notify', mouse_event_fn);

    rubberband.mouseenter('figure_enter', mouse_event_fn);
    rubberband.mouseleave('figure_leave', mouse_event_fn);

    canvas_div.on("wheel", function (event) {
        event = event.originalEvent;
        event['data'] = 'scroll'
        if (event.deltaY < 0) {
            event.step = 1;
        } else {
            event.step = -1;
        }
        mouse_event_fn(event);
    });

    canvas_div.append(canvas);
    canvas_div.append(rubberband);

    this.rubberband = rubberband;
    this.rubberband_canvas = rubberband[0];
    this.rubberband_context = rubberband[0].getContext("2d");
    this.rubberband_context.strokeStyle = "#000000";

    this._resize_canvas = function(width, height) {
        // Keep the size of the canvas, canvas container, and rubber band
        // canvas in synch.
        canvas_div.css('width', width)
        canvas_div.css('height', height)

        canvas.attr('width', width);
        canvas.attr('height', height);

        rubberband.attr('width', width);
        rubberband.attr('height', height);
    }

    // Set the figure to an initial 600x600px, this will subsequently be updated
    // upon first draw.
    this._resize_canvas(600, 600);

    // Disable right mouse context menu.
    $(this.rubberband_canvas).bind("contextmenu",function(e){
        return false;
    });

    function set_focus () {
        canvas.focus();
        canvas_div.focus();
    }

    window.setTimeout(set_focus, 100);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items) {
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) {
            // put a spacer in here.
            continue;
        }
        var button = $('<button/>');
        button.addClass('ui-button ui-widget ui-state-default ui-corner-all ' +
                        'ui-button-icon-only');
        button.attr('role', 'button');
        button.attr('aria-disabled', 'false');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);

        var icon_img = $('<span/>');
        icon_img.addClass('ui-button-icon-primary ui-icon');
        icon_img.addClass(image);
        icon_img.addClass('ui-corner-all');

        var tooltip_span = $('<span/>');
        tooltip_span.addClass('ui-button-text');
        tooltip_span.html(tooltip);

        button.append(icon_img);
        button.append(tooltip_span);

        nav_element.append(button);
    }

    var fmt_picker_span = $('<span/>');

    var fmt_picker = $('<select/>');
    fmt_picker.addClass('mpl-toolbar-option ui-widget ui-widget-content');
    fmt_picker_span.append(fmt_picker);
    nav_element.append(fmt_picker_span);
    this.format_dropdown = fmt_picker[0];

    for (var ind in mpl.extensions) {
        var fmt = mpl.extensions[ind];
        var option = $(
            '<option/>', {selected: fmt === mpl.default_extension}).html(fmt);
        fmt_picker.append(option)
    }

    // Add hover states to the ui-buttons
    $( ".ui-button" ).hover(
        function() { $(this).addClass("ui-state-hover");},
        function() { $(this).removeClass("ui-state-hover");}
    );

    var status_bar = $('<span class="mpl-message"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];
}

mpl.figure.prototype.request_resize = function(x_pixels, y_pixels) {
    // Request matplotlib to resize the figure. Matplotlib will then trigger a resize in the client,
    // which will in turn request a refresh of the image.
    this.send_message('resize', {'width': x_pixels, 'height': y_pixels});
}

mpl.figure.prototype.send_message = function(type, properties) {
    properties['type'] = type;
    properties['figure_id'] = this.id;
    this.ws.send(JSON.stringify(properties));
}

mpl.figure.prototype.send_draw_message = function() {
    if (!this.waiting) {
        this.waiting = true;
        this.ws.send(JSON.stringify({type: "draw", figure_id: this.id}));
    }
}


mpl.figure.prototype.handle_save = function(fig, msg) {
    var format_dropdown = fig.format_dropdown;
    var format = format_dropdown.options[format_dropdown.selectedIndex].value;
    fig.ondownload(fig, format);
}


mpl.figure.prototype.handle_resize = function(fig, msg) {
    var size = msg['size'];
    if (size[0] != fig.canvas.width || size[1] != fig.canvas.height) {
        fig._resize_canvas(size[0], size[1]);
        fig.send_message("refresh", {});
    };
}

mpl.figure.prototype.handle_rubberband = function(fig, msg) {
    var x0 = msg['x0'];
    var y0 = fig.canvas.height - msg['y0'];
    var x1 = msg['x1'];
    var y1 = fig.canvas.height - msg['y1'];
    x0 = Math.floor(x0) + 0.5;
    y0 = Math.floor(y0) + 0.5;
    x1 = Math.floor(x1) + 0.5;
    y1 = Math.floor(y1) + 0.5;
    var min_x = Math.min(x0, x1);
    var min_y = Math.min(y0, y1);
    var width = Math.abs(x1 - x0);
    var height = Math.abs(y1 - y0);

    fig.rubberband_context.clearRect(
        0, 0, fig.canvas.width, fig.canvas.height);

    fig.rubberband_context.strokeRect(min_x, min_y, width, height);
}

mpl.figure.prototype.handle_figure_label = function(fig, msg) {
    // Updates the figure title.
    fig.header.textContent = msg['label'];
}

mpl.figure.prototype.handle_cursor = function(fig, msg) {
    var cursor = msg['cursor'];
    switch(cursor)
    {
    case 0:
        cursor = 'pointer';
        break;
    case 1:
        cursor = 'default';
        break;
    case 2:
        cursor = 'crosshair';
        break;
    case 3:
        cursor = 'move';
        break;
    }
    fig.rubberband_canvas.style.cursor = cursor;
}

mpl.figure.prototype.handle_message = function(fig, msg) {
    fig.message.textContent = msg['message'];
}

mpl.figure.prototype.handle_draw = function(fig, msg) {
    // Request the server to send over a new figure.
    fig.send_draw_message();
}

mpl.figure.prototype.handle_image_mode = function(fig, msg) {
    fig.image_mode = msg['mode'];
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Called whenever the canvas gets updated.
    this.send_message("ack", {});
}

// A function to construct a web socket function for onmessage handling.
// Called in the figure constructor.
mpl.figure.prototype._make_on_message_function = function(fig) {
    return function socket_on_message(evt) {
        if (evt.data instanceof Blob) {
            /* FIXME: We get "Resource interpreted as Image but
             * transferred with MIME type text/plain:" errors on
             * Chrome.  But how to set the MIME type?  It doesn't seem
             * to be part of the websocket stream */
            evt.data.type = "image/png";

            /* Free the memory for the previous frames */
            if (fig.imageObj.src) {
                (window.URL || window.webkitURL).revokeObjectURL(
                    fig.imageObj.src);
            }

            fig.imageObj.src = (window.URL || window.webkitURL).createObjectURL(
                evt.data);
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }
        else if (typeof evt.data === 'string' && evt.data.slice(0, 21) == "data:image/png;base64") {
            fig.imageObj.src = evt.data;
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }

        var msg = JSON.parse(evt.data);
        var msg_type = msg['type'];

        // Call the  "handle_{type}" callback, which takes
        // the figure and JSON message as its only arguments.
        try {
            var callback = fig["handle_" + msg_type];
        } catch (e) {
            console.log("No handler for the '" + msg_type + "' message type: ", msg);
            return;
        }

        if (callback) {
            try {
                // console.log("Handling '" + msg_type + "' message: ", msg);
                callback(fig, msg);
            } catch (e) {
                console.log("Exception inside the 'handler_" + msg_type + "' callback:", e, e.stack, msg);
            }
        }
    };
}

// from http://stackoverflow.com/questions/1114465/getting-mouse-location-in-canvas
mpl.findpos = function(e) {
    //this section is from http://www.quirksmode.org/js/events_properties.html
    var targ;
    if (!e)
        e = window.event;
    if (e.target)
        targ = e.target;
    else if (e.srcElement)
        targ = e.srcElement;
    if (targ.nodeType == 3) // defeat Safari bug
        targ = targ.parentNode;

    // jQuery normalizes the pageX and pageY
    // pageX,Y are the mouse positions relative to the document
    // offset() returns the position of the element relative to the document
    var x = e.pageX - $(targ).offset().left;
    var y = e.pageY - $(targ).offset().top;

    return {"x": x, "y": y};
};

/*
 * return a copy of an object with only non-object keys
 * we need this to avoid circular references
 * http://stackoverflow.com/a/24161582/3208463
 */
function simpleKeys (original) {
  return Object.keys(original).reduce(function (obj, key) {
    if (typeof original[key] !== 'object')
        obj[key] = original[key]
    return obj;
  }, {});
}

mpl.figure.prototype.mouse_event = function(event, name) {
    var canvas_pos = mpl.findpos(event)

    if (name === 'button_press')
    {
        this.canvas.focus();
        this.canvas_div.focus();
    }

    var x = canvas_pos.x;
    var y = canvas_pos.y;

    this.send_message(name, {x: x, y: y, button: event.button,
                             step: event.step,
                             guiEvent: simpleKeys(event)});

    /* This prevents the web browser from automatically changing to
     * the text insertion cursor when the button is pressed.  We want
     * to control all of the cursor setting manually through the
     * 'cursor' event from matplotlib */
    event.preventDefault();
    return false;
}

mpl.figure.prototype._key_event_extra = function(event, name) {
    // Handle any extra behaviour associated with a key event
}

mpl.figure.prototype.key_event = function(event, name) {

    // Prevent repeat events
    if (name == 'key_press')
    {
        if (event.which === this._key)
            return;
        else
            this._key = event.which;
    }
    if (name == 'key_release')
        this._key = null;

    var value = '';
    if (event.ctrlKey && event.which != 17)
        value += "ctrl+";
    if (event.altKey && event.which != 18)
        value += "alt+";
    if (event.shiftKey && event.which != 16)
        value += "shift+";

    value += 'k';
    value += event.which.toString();

    this._key_event_extra(event, name);

    this.send_message(name, {key: value,
                             guiEvent: simpleKeys(event)});
    return false;
}

mpl.figure.prototype.toolbar_button_onclick = function(name) {
    if (name == 'download') {
        this.handle_save(this, null);
    } else {
        this.send_message("toolbar_button", {name: name});
    }
};

mpl.figure.prototype.toolbar_button_onmouseover = function(tooltip) {
    this.message.textContent = tooltip;
};
mpl.toolbar_items = [["Home", "Reset original view", "fa fa-home icon-home", "home"], ["Back", "Back to  previous view", "fa fa-arrow-left icon-arrow-left", "back"], ["Forward", "Forward to next view", "fa fa-arrow-right icon-arrow-right", "forward"], ["", "", "", ""], ["Pan", "Pan axes with left mouse, zoom with right", "fa fa-arrows icon-move", "pan"], ["Zoom", "Zoom to rectangle", "fa fa-square-o icon-check-empty", "zoom"], ["", "", "", ""], ["Download", "Download plot", "fa fa-floppy-o icon-save", "download"]];

mpl.extensions = ["eps", "jpeg", "pdf", "png", "ps", "raw", "svg", "tif"];

mpl.default_extension = "png";var comm_websocket_adapter = function(comm) {
    // Create a "websocket"-like object which calls the given IPython comm
    // object with the appropriate methods. Currently this is a non binary
    // socket, so there is still some room for performance tuning.
    var ws = {};

    ws.close = function() {
        comm.close()
    };
    ws.send = function(m) {
        //console.log('sending', m);
        comm.send(m);
    };
    // Register the callback with on_msg.
    comm.on_msg(function(msg) {
        //console.log('receiving', msg['content']['data'], msg);
        // Pass the mpl event to the overriden (by mpl) onmessage function.
        ws.onmessage(msg['content']['data'])
    });
    return ws;
}

mpl.mpl_figure_comm = function(comm, msg) {
    // This is the function which gets called when the mpl process
    // starts-up an IPython Comm through the "matplotlib" channel.

    var id = msg.content.data.id;
    // Get hold of the div created by the display call when the Comm
    // socket was opened in Python.
    var element = $("#" + id);
    var ws_proxy = comm_websocket_adapter(comm)

    function ondownload(figure, format) {
        window.open(figure.imageObj.src);
    }

    var fig = new mpl.figure(id, ws_proxy,
                           ondownload,
                           element.get(0));

    // Call onopen now - mpl needs it, as it is assuming we've passed it a real
    // web socket which is closed, not our websocket->open comm proxy.
    ws_proxy.onopen();

    fig.parent_element = element.get(0);
    fig.cell_info = mpl.find_output_cell("<div id='" + id + "'></div>");
    if (!fig.cell_info) {
        console.error("Failed to find cell for figure", id, fig);
        return;
    }

    var output_index = fig.cell_info[2]
    var cell = fig.cell_info[0];

};

mpl.figure.prototype.handle_close = function(fig, msg) {
    fig.root.unbind('remove')

    // Update the output cell to use the data from the current canvas.
    fig.push_to_output();
    var dataURL = fig.canvas.toDataURL();
    // Re-enable the keyboard manager in IPython - without this line, in FF,
    // the notebook keyboard shortcuts fail.
    IPython.keyboard_manager.enable()
    $(fig.parent_element).html('<img src="' + dataURL + '">');
    fig.close_ws(fig, msg);
}

mpl.figure.prototype.close_ws = function(fig, msg){
    fig.send_message('closing', msg);
    // fig.ws.close()
}

mpl.figure.prototype.push_to_output = function(remove_interactive) {
    // Turn the data on the canvas into data in the output cell.
    var dataURL = this.canvas.toDataURL();
    this.cell_info[1]['text/html'] = '<img src="' + dataURL + '">';
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Tell IPython that the notebook contents must change.
    IPython.notebook.set_dirty(true);
    this.send_message("ack", {});
    var fig = this;
    // Wait a second, then push the new image to the DOM so
    // that it is saved nicely (might be nice to debounce this).
    setTimeout(function () { fig.push_to_output() }, 1000);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items){
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) { continue; };

        var button = $('<button class="btn btn-default" href="#" title="' + name + '"><i class="fa ' + image + ' fa-lg"></i></button>');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);
        nav_element.append(button);
    }

    // Add the status bar.
    var status_bar = $('<span class="mpl-message" style="text-align:right; float: right;"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];

    // Add the close button to the window.
    var buttongrp = $('<div class="btn-group inline pull-right"></div>');
    var button = $('<button class="btn btn-mini btn-primary" href="#" title="Stop Interaction"><i class="fa fa-power-off icon-remove icon-large"></i></button>');
    button.click(function (evt) { fig.handle_close(fig, {}); } );
    button.mouseover('Stop Interaction', toolbar_mouse_event);
    buttongrp.append(button);
    var titlebar = this.root.find($('.ui-dialog-titlebar'));
    titlebar.prepend(buttongrp);
}

mpl.figure.prototype._root_extra_style = function(el){
    var fig = this
    el.on("remove", function(){
	fig.close_ws(fig, {});
    });
}

mpl.figure.prototype._canvas_extra_style = function(el){
    // this is important to make the div 'focusable
    el.attr('tabindex', 0)
    // reach out to IPython and tell the keyboard manager to turn it's self
    // off when our div gets focus

    // location in version 3
    if (IPython.notebook.keyboard_manager) {
        IPython.notebook.keyboard_manager.register_events(el);
    }
    else {
        // location in version 2
        IPython.keyboard_manager.register_events(el);
    }

}

mpl.figure.prototype._key_event_extra = function(event, name) {
    var manager = IPython.notebook.keyboard_manager;
    if (!manager)
        manager = IPython.keyboard_manager;

    // Check for shift+enter
    if (event.shiftKey && event.which == 13) {
        this.canvas_div.blur();
        event.shiftKey = false;
        // Send a "J" for go to next cell
        event.which = 74;
        event.keyCode = 74;
        manager.command_mode();
        manager.handle_keydown(event);
    }
}

mpl.figure.prototype.handle_save = function(fig, msg) {
    fig.ondownload(fig, null);
}


mpl.find_output_cell = function(html_output) {
    // Return the cell and output element which can be found *uniquely* in the notebook.
    // Note - this is a bit hacky, but it is done because the "notebook_saving.Notebook"
    // IPython event is triggered only after the cells have been serialised, which for
    // our purposes (turning an active figure into a static one), is too late.
    var cells = IPython.notebook.get_cells();
    var ncells = cells.length;
    for (var i=0; i<ncells; i++) {
        var cell = cells[i];
        if (cell.cell_type === 'code'){
            for (var j=0; j<cell.output_area.outputs.length; j++) {
                var data = cell.output_area.outputs[j];
                if (data.data) {
                    // IPython >= 3 moved mimebundle to data attribute of output
                    data = data.data;
                }
                if (data['text/html'] == html_output) {
                    return [cell, data, j];
                }
            }
        }
    }
}

// Register the function which deals with the matplotlib target/channel.
// The kernel may be null if the page has been refreshed.
if (IPython.notebook.kernel != null) {
    IPython.notebook.kernel.comm_manager.register_target('matplotlib', mpl.mpl_figure_comm);
}

</script>
</div>

</div>

<div class="output_area"><div class="prompt"></div>

<div class="output_html rendered_html output_subarea ">
<img src="data:image/png;base64,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">
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>b. What can you infer from the charts? In what region is advertising most effective?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>For the test group users, the conversion rates were generally higher for the users that saw more impressions.  Test users that were exposed to greater than 1400 impressions had conversion rates of at least 40%. However, only about 6 users saw that amount of impressions. That is statistically insignificant so we regard them as outliers and exclude those 6 cases from this analysis.</p>
<p>Users exposed to a minimum of 100 and a maximum of 1400 impressions showed a relatively steady conversion rates. They had an average conversion rate of 15.36%. But once again, there were not that many users in the higher end of that range to conclude confidently. If we limit the range to between 100 and 800 impressions, the conversion rate increases to 17.03% for a relatively significant number of users (about 4%). If we limit the range further to between 100 and 400 impressions for better statistical confidence, the conversion rate drops to 15.86%.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We can conclude that advertising was most effective for users that were exposed to a minimum of 100 impressions and a maximum of 400 impressions. Below 100, the conversion rates fall significantly to about 1.96% which is where most users fall and also closest to the overall conversion rate. Above 400, there are issues of statistical significance and cost diminishing returns.</p>
<p>For the control group users, we can’t make any inference about the effectiveness of the advertising since they were not exposed to the actual product advertisement. However, it was interesting to note that for control group users exposed to a minimum of 100 and a maximum of 600 impressions, there was an average conversion rate of about 14% compared to 1.33% for users exposed to a maximum of 100 impressions. This could be due to statistical insignificance.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>c. What do the above figures imply for the design of the next campaign assuming that consumer response would be similar?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The 0 – 1300 range of impressions sent lead to conversion rates between the range of 0% - 20%.
The 0 – 1200 has a few anomalies. One notable one was the 1200 – 1300 range of impressions having a 0% conversion rate though the range only had 3 cases (small sample). Also the range of 700 – 800 impressions goes above the 20% conversion margin with a 21.176471% conversion. When we look at the average conversion rate within the 0 – 1300 range it is only at 2.523%. This is because most of the users were sent impressions within the 0 – 100 range (which has the most accurate representation of conversion rate at 1.96%). It is statistically significant to note that the 0 – 100 range has the largest sample size. It is also important to note that range 100 – 200 is also statistically significant with 17517 samples. 
The 1300 - 1700 range of impressions sent leads to conversion rates within the 40% to 60% range (for impressions of range 1500 - 1600, no case existed). 
The 1300 – 1700 range has an average rate of conversion of 45.45%. It is important to note that this range of impressions has a low sample size.
The 1700 - 1800 range of impressions sent has a 100% conversion rate, although this range has a very small sample size (only one case existed)
For impressions sent greater than 1800 only one case exists (2065 impressions sent) but this user was not converted. However this case is statistically insignificant due to sample size.</p>
<p>Under the assumption that the next campaign will result in similar consumer response; we can find the optimal “range of impressions sent” to target that will give us the best value in terms of expected profit from each range. 
The expected profit per individual from each of the ranges is equal to 40 * conversion%</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="https://imgbb.com/"><img src="https://image.ibb.co/d3BrSR/q3table2.png" alt="q3table2" border="0" /></a></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The cost of each impression sent is equal to $9/cpm (cost per thousand) which would equal 0.009 per impression
By taking the middle value of each range (eg. 150 for the 100 – 200 range) and multiplying that value by the cost of each impression, we would get the typical cost of the aforementioned range of impressions that we as a company can send. 
Then by subtracting our calculated value from the expected value of conversion we can find the expected net profit of impressions sent. By comparing the rates we can find which range of targets has the best value.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="https://imgbb.com/"><img src="https://image.ibb.co/kf0exR/table3c.png" alt="table3c" border="0" /></a></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The range that gives us the best expected net profit of impressions sent is the 100 – 200 range. What this number means is that if we send 150 impressions to an individual, the expected value we gain from that action is equal to $5.721. As stated earlier the 100 – 200 range is statistically significant as well, with a sample size of 17517. For our next campaign we should design our advertisement targets, so that each individual will be exposed to between 100 to 200 impressions.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="4.-How-does-consumer-response-to-advertising-vary-on-different-days-of-the-week-and-at-different-times-of-the-day?">4. How does consumer response to advertising vary on different days of the week and at different times of the day?<a class="anchor-link" href="#4.-How-does-consumer-response-to-advertising-vary-on-different-days-of-the-week-and-at-different-times-of-the-day?">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>a. Create a chart with the conversion rates for the control group and the exposed group as a function of the day of week when they were shown the most impressions.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[29]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython2"><pre><span class="c"># Plot mode_impr_day vs conversion rate:</span>

<span class="n">g3</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s">&quot;mode_impr_day&quot;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s">&quot;converted&quot;</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s">&quot;test&quot;</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">df</span><span class="p">)</span>
<span class="n">g3</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s">&#39;Mode Impression Days vs. Conversion Rates&#39;</span><span class="p">)</span>
<span class="n">g3</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s">&#39;Days&#39;</span><span class="p">)</span>
<span class="n">g3</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s">&#39;Conversion Rates (%)&#39;</span><span class="p">)</span>
<span class="n">g3</span><span class="o">.</span><span class="n">set_xticklabels</span><span class="p">([</span><span class="s">&#39;Monday&#39;</span><span class="p">,</span> <span class="s">&#39;Tuesday&#39;</span><span class="p">,</span> <span class="s">&#39;Wednesday&#39;</span><span class="p">,</span> <span class="s">&#39;Thursday&#39;</span><span class="p">,</span> <span class="s">&#39;Friday&#39;</span><span class="p">,</span> <span class="s">&#39;Saturday&#39;</span><span class="p">,</span> <span class="s">&#39;Sunday&#39;</span><span class="p">])</span>
<span class="n">g3</span><span class="o">.</span><span class="n">set_yticklabels</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mf">0.5</span><span class="p">))</span>
<span class="n">g3</span><span class="o">.</span><span class="n">legend_</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s">&#39;Group:&#39;</span><span class="p">)</span>
<span class="k">for</span> <span class="n">t</span><span class="p">,</span> <span class="n">l</span> <span class="ow">in</span> <span class="nb">zip</span><span class="p">(</span><span class="n">g3</span><span class="o">.</span><span class="n">legend_</span><span class="o">.</span><span class="n">texts</span><span class="p">,</span> <span class="p">[</span><span class="s">&#39;Control&#39;</span><span class="p">,</span> <span class="s">&#39;Test&#39;</span><span class="p">]):</span> <span class="n">t</span><span class="o">.</span><span class="n">set_text</span><span class="p">(</span><span class="n">l</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>


<div class="output_subarea output_javascript ">
<script type="text/javascript">
/* Put everything inside the global mpl namespace */
window.mpl = {};

mpl.get_websocket_type = function() {
    if (typeof(WebSocket) !== 'undefined') {
        return WebSocket;
    } else if (typeof(MozWebSocket) !== 'undefined') {
        return MozWebSocket;
    } else {
        alert('Your browser does not have WebSocket support.' +
              'Please try Chrome, Safari or Firefox ≥ 6. ' +
              'Firefox 4 and 5 are also supported but you ' +
              'have to enable WebSockets in about:config.');
    };
}

mpl.figure = function(figure_id, websocket, ondownload, parent_element) {
    this.id = figure_id;

    this.ws = websocket;

    this.supports_binary = (this.ws.binaryType != undefined);

    if (!this.supports_binary) {
        var warnings = document.getElementById("mpl-warnings");
        if (warnings) {
            warnings.style.display = 'block';
            warnings.textContent = (
                "This browser does not support binary websocket messages. " +
                    "Performance may be slow.");
        }
    }

    this.imageObj = new Image();

    this.context = undefined;
    this.message = undefined;
    this.canvas = undefined;
    this.rubberband_canvas = undefined;
    this.rubberband_context = undefined;
    this.format_dropdown = undefined;

    this.image_mode = 'full';

    this.root = $('<div/>');
    this._root_extra_style(this.root)
    this.root.attr('style', 'display: inline-block');

    $(parent_element).append(this.root);

    this._init_header(this);
    this._init_canvas(this);
    this._init_toolbar(this);

    var fig = this;

    this.waiting = false;

    this.ws.onopen =  function () {
            fig.send_message("supports_binary", {value: fig.supports_binary});
            fig.send_message("send_image_mode", {});
            fig.send_message("refresh", {});
        }

    this.imageObj.onload = function() {
            if (fig.image_mode == 'full') {
                // Full images could contain transparency (where diff images
                // almost always do), so we need to clear the canvas so that
                // there is no ghosting.
                fig.context.clearRect(0, 0, fig.canvas.width, fig.canvas.height);
            }
            fig.context.drawImage(fig.imageObj, 0, 0);
        };

    this.imageObj.onunload = function() {
        this.ws.close();
    }

    this.ws.onmessage = this._make_on_message_function(this);

    this.ondownload = ondownload;
}

mpl.figure.prototype._init_header = function() {
    var titlebar = $(
        '<div class="ui-dialog-titlebar ui-widget-header ui-corner-all ' +
        'ui-helper-clearfix"/>');
    var titletext = $(
        '<div class="ui-dialog-title" style="width: 100%; ' +
        'text-align: center; padding: 3px;"/>');
    titlebar.append(titletext)
    this.root.append(titlebar);
    this.header = titletext[0];
}



mpl.figure.prototype._canvas_extra_style = function(canvas_div) {

}


mpl.figure.prototype._root_extra_style = function(canvas_div) {

}

mpl.figure.prototype._init_canvas = function() {
    var fig = this;

    var canvas_div = $('<div/>');

    canvas_div.attr('style', 'position: relative; clear: both; outline: 0');

    function canvas_keyboard_event(event) {
        return fig.key_event(event, event['data']);
    }

    canvas_div.keydown('key_press', canvas_keyboard_event);
    canvas_div.keyup('key_release', canvas_keyboard_event);
    this.canvas_div = canvas_div
    this._canvas_extra_style(canvas_div)
    this.root.append(canvas_div);

    var canvas = $('<canvas/>');
    canvas.addClass('mpl-canvas');
    canvas.attr('style', "left: 0; top: 0; z-index: 0; outline: 0")

    this.canvas = canvas[0];
    this.context = canvas[0].getContext("2d");

    var rubberband = $('<canvas/>');
    rubberband.attr('style', "position: absolute; left: 0; top: 0; z-index: 1;")

    var pass_mouse_events = true;

    canvas_div.resizable({
        start: function(event, ui) {
            pass_mouse_events = false;
        },
        resize: function(event, ui) {
            fig.request_resize(ui.size.width, ui.size.height);
        },
        stop: function(event, ui) {
            pass_mouse_events = true;
            fig.request_resize(ui.size.width, ui.size.height);
        },
    });

    function mouse_event_fn(event) {
        if (pass_mouse_events)
            return fig.mouse_event(event, event['data']);
    }

    rubberband.mousedown('button_press', mouse_event_fn);
    rubberband.mouseup('button_release', mouse_event_fn);
    // Throttle sequential mouse events to 1 every 20ms.
    rubberband.mousemove('motion_notify', mouse_event_fn);

    rubberband.mouseenter('figure_enter', mouse_event_fn);
    rubberband.mouseleave('figure_leave', mouse_event_fn);

    canvas_div.on("wheel", function (event) {
        event = event.originalEvent;
        event['data'] = 'scroll'
        if (event.deltaY < 0) {
            event.step = 1;
        } else {
            event.step = -1;
        }
        mouse_event_fn(event);
    });

    canvas_div.append(canvas);
    canvas_div.append(rubberband);

    this.rubberband = rubberband;
    this.rubberband_canvas = rubberband[0];
    this.rubberband_context = rubberband[0].getContext("2d");
    this.rubberband_context.strokeStyle = "#000000";

    this._resize_canvas = function(width, height) {
        // Keep the size of the canvas, canvas container, and rubber band
        // canvas in synch.
        canvas_div.css('width', width)
        canvas_div.css('height', height)

        canvas.attr('width', width);
        canvas.attr('height', height);

        rubberband.attr('width', width);
        rubberband.attr('height', height);
    }

    // Set the figure to an initial 600x600px, this will subsequently be updated
    // upon first draw.
    this._resize_canvas(600, 600);

    // Disable right mouse context menu.
    $(this.rubberband_canvas).bind("contextmenu",function(e){
        return false;
    });

    function set_focus () {
        canvas.focus();
        canvas_div.focus();
    }

    window.setTimeout(set_focus, 100);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items) {
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) {
            // put a spacer in here.
            continue;
        }
        var button = $('<button/>');
        button.addClass('ui-button ui-widget ui-state-default ui-corner-all ' +
                        'ui-button-icon-only');
        button.attr('role', 'button');
        button.attr('aria-disabled', 'false');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);

        var icon_img = $('<span/>');
        icon_img.addClass('ui-button-icon-primary ui-icon');
        icon_img.addClass(image);
        icon_img.addClass('ui-corner-all');

        var tooltip_span = $('<span/>');
        tooltip_span.addClass('ui-button-text');
        tooltip_span.html(tooltip);

        button.append(icon_img);
        button.append(tooltip_span);

        nav_element.append(button);
    }

    var fmt_picker_span = $('<span/>');

    var fmt_picker = $('<select/>');
    fmt_picker.addClass('mpl-toolbar-option ui-widget ui-widget-content');
    fmt_picker_span.append(fmt_picker);
    nav_element.append(fmt_picker_span);
    this.format_dropdown = fmt_picker[0];

    for (var ind in mpl.extensions) {
        var fmt = mpl.extensions[ind];
        var option = $(
            '<option/>', {selected: fmt === mpl.default_extension}).html(fmt);
        fmt_picker.append(option)
    }

    // Add hover states to the ui-buttons
    $( ".ui-button" ).hover(
        function() { $(this).addClass("ui-state-hover");},
        function() { $(this).removeClass("ui-state-hover");}
    );

    var status_bar = $('<span class="mpl-message"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];
}

mpl.figure.prototype.request_resize = function(x_pixels, y_pixels) {
    // Request matplotlib to resize the figure. Matplotlib will then trigger a resize in the client,
    // which will in turn request a refresh of the image.
    this.send_message('resize', {'width': x_pixels, 'height': y_pixels});
}

mpl.figure.prototype.send_message = function(type, properties) {
    properties['type'] = type;
    properties['figure_id'] = this.id;
    this.ws.send(JSON.stringify(properties));
}

mpl.figure.prototype.send_draw_message = function() {
    if (!this.waiting) {
        this.waiting = true;
        this.ws.send(JSON.stringify({type: "draw", figure_id: this.id}));
    }
}


mpl.figure.prototype.handle_save = function(fig, msg) {
    var format_dropdown = fig.format_dropdown;
    var format = format_dropdown.options[format_dropdown.selectedIndex].value;
    fig.ondownload(fig, format);
}


mpl.figure.prototype.handle_resize = function(fig, msg) {
    var size = msg['size'];
    if (size[0] != fig.canvas.width || size[1] != fig.canvas.height) {
        fig._resize_canvas(size[0], size[1]);
        fig.send_message("refresh", {});
    };
}

mpl.figure.prototype.handle_rubberband = function(fig, msg) {
    var x0 = msg['x0'];
    var y0 = fig.canvas.height - msg['y0'];
    var x1 = msg['x1'];
    var y1 = fig.canvas.height - msg['y1'];
    x0 = Math.floor(x0) + 0.5;
    y0 = Math.floor(y0) + 0.5;
    x1 = Math.floor(x1) + 0.5;
    y1 = Math.floor(y1) + 0.5;
    var min_x = Math.min(x0, x1);
    var min_y = Math.min(y0, y1);
    var width = Math.abs(x1 - x0);
    var height = Math.abs(y1 - y0);

    fig.rubberband_context.clearRect(
        0, 0, fig.canvas.width, fig.canvas.height);

    fig.rubberband_context.strokeRect(min_x, min_y, width, height);
}

mpl.figure.prototype.handle_figure_label = function(fig, msg) {
    // Updates the figure title.
    fig.header.textContent = msg['label'];
}

mpl.figure.prototype.handle_cursor = function(fig, msg) {
    var cursor = msg['cursor'];
    switch(cursor)
    {
    case 0:
        cursor = 'pointer';
        break;
    case 1:
        cursor = 'default';
        break;
    case 2:
        cursor = 'crosshair';
        break;
    case 3:
        cursor = 'move';
        break;
    }
    fig.rubberband_canvas.style.cursor = cursor;
}

mpl.figure.prototype.handle_message = function(fig, msg) {
    fig.message.textContent = msg['message'];
}

mpl.figure.prototype.handle_draw = function(fig, msg) {
    // Request the server to send over a new figure.
    fig.send_draw_message();
}

mpl.figure.prototype.handle_image_mode = function(fig, msg) {
    fig.image_mode = msg['mode'];
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Called whenever the canvas gets updated.
    this.send_message("ack", {});
}

// A function to construct a web socket function for onmessage handling.
// Called in the figure constructor.
mpl.figure.prototype._make_on_message_function = function(fig) {
    return function socket_on_message(evt) {
        if (evt.data instanceof Blob) {
            /* FIXME: We get "Resource interpreted as Image but
             * transferred with MIME type text/plain:" errors on
             * Chrome.  But how to set the MIME type?  It doesn't seem
             * to be part of the websocket stream */
            evt.data.type = "image/png";

            /* Free the memory for the previous frames */
            if (fig.imageObj.src) {
                (window.URL || window.webkitURL).revokeObjectURL(
                    fig.imageObj.src);
            }

            fig.imageObj.src = (window.URL || window.webkitURL).createObjectURL(
                evt.data);
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }
        else if (typeof evt.data === 'string' && evt.data.slice(0, 21) == "data:image/png;base64") {
            fig.imageObj.src = evt.data;
            fig.updated_canvas_event();
            fig.waiting = false;
            return;
        }

        var msg = JSON.parse(evt.data);
        var msg_type = msg['type'];

        // Call the  "handle_{type}" callback, which takes
        // the figure and JSON message as its only arguments.
        try {
            var callback = fig["handle_" + msg_type];
        } catch (e) {
            console.log("No handler for the '" + msg_type + "' message type: ", msg);
            return;
        }

        if (callback) {
            try {
                // console.log("Handling '" + msg_type + "' message: ", msg);
                callback(fig, msg);
            } catch (e) {
                console.log("Exception inside the 'handler_" + msg_type + "' callback:", e, e.stack, msg);
            }
        }
    };
}

// from http://stackoverflow.com/questions/1114465/getting-mouse-location-in-canvas
mpl.findpos = function(e) {
    //this section is from http://www.quirksmode.org/js/events_properties.html
    var targ;
    if (!e)
        e = window.event;
    if (e.target)
        targ = e.target;
    else if (e.srcElement)
        targ = e.srcElement;
    if (targ.nodeType == 3) // defeat Safari bug
        targ = targ.parentNode;

    // jQuery normalizes the pageX and pageY
    // pageX,Y are the mouse positions relative to the document
    // offset() returns the position of the element relative to the document
    var x = e.pageX - $(targ).offset().left;
    var y = e.pageY - $(targ).offset().top;

    return {"x": x, "y": y};
};

/*
 * return a copy of an object with only non-object keys
 * we need this to avoid circular references
 * http://stackoverflow.com/a/24161582/3208463
 */
function simpleKeys (original) {
  return Object.keys(original).reduce(function (obj, key) {
    if (typeof original[key] !== 'object')
        obj[key] = original[key]
    return obj;
  }, {});
}

mpl.figure.prototype.mouse_event = function(event, name) {
    var canvas_pos = mpl.findpos(event)

    if (name === 'button_press')
    {
        this.canvas.focus();
        this.canvas_div.focus();
    }

    var x = canvas_pos.x;
    var y = canvas_pos.y;

    this.send_message(name, {x: x, y: y, button: event.button,
                             step: event.step,
                             guiEvent: simpleKeys(event)});

    /* This prevents the web browser from automatically changing to
     * the text insertion cursor when the button is pressed.  We want
     * to control all of the cursor setting manually through the
     * 'cursor' event from matplotlib */
    event.preventDefault();
    return false;
}

mpl.figure.prototype._key_event_extra = function(event, name) {
    // Handle any extra behaviour associated with a key event
}

mpl.figure.prototype.key_event = function(event, name) {

    // Prevent repeat events
    if (name == 'key_press')
    {
        if (event.which === this._key)
            return;
        else
            this._key = event.which;
    }
    if (name == 'key_release')
        this._key = null;

    var value = '';
    if (event.ctrlKey && event.which != 17)
        value += "ctrl+";
    if (event.altKey && event.which != 18)
        value += "alt+";
    if (event.shiftKey && event.which != 16)
        value += "shift+";

    value += 'k';
    value += event.which.toString();

    this._key_event_extra(event, name);

    this.send_message(name, {key: value,
                             guiEvent: simpleKeys(event)});
    return false;
}

mpl.figure.prototype.toolbar_button_onclick = function(name) {
    if (name == 'download') {
        this.handle_save(this, null);
    } else {
        this.send_message("toolbar_button", {name: name});
    }
};

mpl.figure.prototype.toolbar_button_onmouseover = function(tooltip) {
    this.message.textContent = tooltip;
};
mpl.toolbar_items = [["Home", "Reset original view", "fa fa-home icon-home", "home"], ["Back", "Back to  previous view", "fa fa-arrow-left icon-arrow-left", "back"], ["Forward", "Forward to next view", "fa fa-arrow-right icon-arrow-right", "forward"], ["", "", "", ""], ["Pan", "Pan axes with left mouse, zoom with right", "fa fa-arrows icon-move", "pan"], ["Zoom", "Zoom to rectangle", "fa fa-square-o icon-check-empty", "zoom"], ["", "", "", ""], ["Download", "Download plot", "fa fa-floppy-o icon-save", "download"]];

mpl.extensions = ["eps", "jpeg", "pdf", "png", "ps", "raw", "svg", "tif"];

mpl.default_extension = "png";var comm_websocket_adapter = function(comm) {
    // Create a "websocket"-like object which calls the given IPython comm
    // object with the appropriate methods. Currently this is a non binary
    // socket, so there is still some room for performance tuning.
    var ws = {};

    ws.close = function() {
        comm.close()
    };
    ws.send = function(m) {
        //console.log('sending', m);
        comm.send(m);
    };
    // Register the callback with on_msg.
    comm.on_msg(function(msg) {
        //console.log('receiving', msg['content']['data'], msg);
        // Pass the mpl event to the overriden (by mpl) onmessage function.
        ws.onmessage(msg['content']['data'])
    });
    return ws;
}

mpl.mpl_figure_comm = function(comm, msg) {
    // This is the function which gets called when the mpl process
    // starts-up an IPython Comm through the "matplotlib" channel.

    var id = msg.content.data.id;
    // Get hold of the div created by the display call when the Comm
    // socket was opened in Python.
    var element = $("#" + id);
    var ws_proxy = comm_websocket_adapter(comm)

    function ondownload(figure, format) {
        window.open(figure.imageObj.src);
    }

    var fig = new mpl.figure(id, ws_proxy,
                           ondownload,
                           element.get(0));

    // Call onopen now - mpl needs it, as it is assuming we've passed it a real
    // web socket which is closed, not our websocket->open comm proxy.
    ws_proxy.onopen();

    fig.parent_element = element.get(0);
    fig.cell_info = mpl.find_output_cell("<div id='" + id + "'></div>");
    if (!fig.cell_info) {
        console.error("Failed to find cell for figure", id, fig);
        return;
    }

    var output_index = fig.cell_info[2]
    var cell = fig.cell_info[0];

};

mpl.figure.prototype.handle_close = function(fig, msg) {
    fig.root.unbind('remove')

    // Update the output cell to use the data from the current canvas.
    fig.push_to_output();
    var dataURL = fig.canvas.toDataURL();
    // Re-enable the keyboard manager in IPython - without this line, in FF,
    // the notebook keyboard shortcuts fail.
    IPython.keyboard_manager.enable()
    $(fig.parent_element).html('<img src="' + dataURL + '">');
    fig.close_ws(fig, msg);
}

mpl.figure.prototype.close_ws = function(fig, msg){
    fig.send_message('closing', msg);
    // fig.ws.close()
}

mpl.figure.prototype.push_to_output = function(remove_interactive) {
    // Turn the data on the canvas into data in the output cell.
    var dataURL = this.canvas.toDataURL();
    this.cell_info[1]['text/html'] = '<img src="' + dataURL + '">';
}

mpl.figure.prototype.updated_canvas_event = function() {
    // Tell IPython that the notebook contents must change.
    IPython.notebook.set_dirty(true);
    this.send_message("ack", {});
    var fig = this;
    // Wait a second, then push the new image to the DOM so
    // that it is saved nicely (might be nice to debounce this).
    setTimeout(function () { fig.push_to_output() }, 1000);
}

mpl.figure.prototype._init_toolbar = function() {
    var fig = this;

    var nav_element = $('<div/>')
    nav_element.attr('style', 'width: 100%');
    this.root.append(nav_element);

    // Define a callback function for later on.
    function toolbar_event(event) {
        return fig.toolbar_button_onclick(event['data']);
    }
    function toolbar_mouse_event(event) {
        return fig.toolbar_button_onmouseover(event['data']);
    }

    for(var toolbar_ind in mpl.toolbar_items){
        var name = mpl.toolbar_items[toolbar_ind][0];
        var tooltip = mpl.toolbar_items[toolbar_ind][1];
        var image = mpl.toolbar_items[toolbar_ind][2];
        var method_name = mpl.toolbar_items[toolbar_ind][3];

        if (!name) { continue; };

        var button = $('<button class="btn btn-default" href="#" title="' + name + '"><i class="fa ' + image + ' fa-lg"></i></button>');
        button.click(method_name, toolbar_event);
        button.mouseover(tooltip, toolbar_mouse_event);
        nav_element.append(button);
    }

    // Add the status bar.
    var status_bar = $('<span class="mpl-message" style="text-align:right; float: right;"/>');
    nav_element.append(status_bar);
    this.message = status_bar[0];

    // Add the close button to the window.
    var buttongrp = $('<div class="btn-group inline pull-right"></div>');
    var button = $('<button class="btn btn-mini btn-primary" href="#" title="Stop Interaction"><i class="fa fa-power-off icon-remove icon-large"></i></button>');
    button.click(function (evt) { fig.handle_close(fig, {}); } );
    button.mouseover('Stop Interaction', toolbar_mouse_event);
    buttongrp.append(button);
    var titlebar = this.root.find($('.ui-dialog-titlebar'));
    titlebar.prepend(buttongrp);
}

mpl.figure.prototype._root_extra_style = function(el){
    var fig = this
    el.on("remove", function(){
	fig.close_ws(fig, {});
    });
}

mpl.figure.prototype._canvas_extra_style = function(el){
    // this is important to make the div 'focusable
    el.attr('tabindex', 0)
    // reach out to IPython and tell the keyboard manager to turn it's self
    // off when our div gets focus

    // location in version 3
    if (IPython.notebook.keyboard_manager) {
        IPython.notebook.keyboard_manager.register_events(el);
    }
    else {
        // location in version 2
        IPython.keyboard_manager.register_events(el);
    }

}

mpl.figure.prototype._key_event_extra = function(event, name) {
    var manager = IPython.notebook.keyboard_manager;
    if (!manager)
        manager = IPython.keyboard_manager;

    // Check for shift+enter
    if (event.shiftKey && event.which == 13) {
        this.canvas_div.blur();
        event.shiftKey = false;
        // Send a "J" for go to next cell
        event.which = 74;
        event.keyCode = 74;
        manager.command_mode();
        manager.handle_keydown(event);
    }
}

mpl.figure.prototype.handle_save = function(fig, msg) {
    fig.ondownload(fig, null);
}


mpl.find_output_cell = function(html_output) {
    // Return the cell and output element which can be found *uniquely* in the notebook.
    // Note - this is a bit hacky, but it is done because the "notebook_saving.Notebook"
    // IPython event is triggered only after the cells have been serialised, which for
    // our purposes (turning an active figure into a static one), is too late.
    var cells = IPython.notebook.get_cells();
    var ncells = cells.length;
    for (var i=0; i<ncells; i++) {
        var cell = cells[i];
        if (cell.cell_type === 'code'){
            for (var j=0; j<cell.output_area.outputs.length; j++) {
                var data = cell.output_area.outputs[j];
                if (data.data) {
                    // IPython >= 3 moved mimebundle to data attribute of output
                    data = data.data;
                }
                if (data['text/html'] == html_output) {
                    return [cell, data, j];
                }
            }
        }
    }
}

// Register the function which deals with the matplotlib target/channel.
// The kernel may be null if the page has been refreshed.
if (IPython.notebook.kernel != null) {
    IPython.notebook.kernel.comm_manager.register_target('matplotlib', mpl.mpl_figure_comm);
}

</script>
</div>

</div>

<div class="output_area"><div class="prompt"></div>

<div class="output_html rendered_html output_subarea ">
