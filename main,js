$( document ).ready(function() {
  rtlCheck(".TaskDescription-textEditor");
  rtlCheck(".truncatedRichText");
  rtlCheck(".CommentComposer");
});

/*functions definition*/
function rtlCheck(selector){
  $("body").on('DOMSubtreeModified', '.SingleTaskPane', function(){
    $(selector).each(function(){
      var position = $(this).text().search(/[\u0590-\u05FF]/);
      if(position >= 0){
          console.log('a: '+this+' contains Hebrew');
        $(this).css('direction','rtl');
        }else{
        $(this).css('direction','ltr');
        console.log('a: '+this+' contains English');
      }
    });
  });
}
