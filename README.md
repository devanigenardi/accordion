# accordion
accordion


<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
  <style>
    .category--holder a::before {
      content: 'cbdjs'
    }

    .category--holder p {
      display: none;
    }

    .active {
      color: red;
    }
  </style>
</head>
<body>
  
  <div class="accordion__category--holder">
  
    <div class="category--holder">
      <a href="#">open ietm</a>
      <p>this is the content</p>
    </div>
    
    <div class="category--holder">
      <a href="#">open ietm</a>
      <p>this is the content</p>
    </div>
    
    <div class="category--holder">
      <a href="#">open ietm</a>
      <p>this is the content</p>
    </div>
    
  </div>
  
  <div>
    <a class="close-all" href="#">close all elements</a>
    <a class="open-all" href="#">open all elements</a>
  </div>

</body>
<script src="https://code.jquery.com/jquery-3.1.0.js"></script>
<script>

  $(document).ready(function(){
  
  	var interval = 200;
  
  	$('.category--holder a').on('click', function(){
    	$(this).toggleClass('active');
    	$(this).next().toggle(interval);
    });
    
    $('.close-all').on('click', function(){
    	$('.category--holder p').hide(interval);
      $('.category--holder a').removeClass('active');
    });
    $('.open-all').on('click', function(){
    	$('.category--holder p').show(interval);
      $('.category--holder a').addClass('active');
    });
 
  });
  
</script>
</html>
