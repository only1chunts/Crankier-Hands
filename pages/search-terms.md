
<head>
  <meta charset="UTF-8">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
</head>
<body>
  <div>
    <h1>Term Search</h1>
	<div id="header"></div>
	<div>
Here we provide a simple search tool to assist finding particular items.<br>
	</div>
	<form role="form">
        <div class="form-group">
          <input type="input" class="form-control input-lg" id="txt-search" placeholder="Start typing to searh">
        </div>
	</form>
	<div id="filter-records"></div>
	<div id="footer"></div>
  </div>
</body>

<script type="text/javascript">
  $(document).ready(function(){

    var data = 
{% for-sale.yml %}
;

$('#txt-search').keyup(function(){
            var searchField = $(this).val();
			if(searchField === '')  {
				$('#filter-records').html('');
				return;
			}
			
            var regex = new RegExp(searchField, "i");
            var output = '<div class="row">';
            var count = 1;
			  $.each(data, function(key, val){
				if ((val.item.search(regex) != -1) || (val.label.search(regex) != -1) || (val.definition.search(regex) != -1)) {
				  output += '<h5>' +val.item+ '</h5>'; 
				  output += '<strong>Definition: </strong>' + val.definition + '</br>';
				  if(count%2 == 0){
					output += '</div><div class="row">'
				  }
				  count++;
				}
			  });
			  output += '</div>';
			  $('#filter-records').html(output);
        });
  });
</script>