# Tapşırıq

Aşağıdakı əməliyyatları edə bilməyimiz üçün 3 fərqli funksiya yazın. (hər bir əməliyyat üçün ayrıca funksiya)
- from decimal to binary
- from decimal to hexadecimal
- is given number perfectu

1. From decimal to binary. 
		
<script>
	function IkiliSay(number){
		var result=[],i;
		for (i=number; i>0; i=parseInt(i/2)) {
			result.push(i%2);
		}
	return result.reverse().join("");
	}
	document.write("OnluqSay(10)=IkiliSay:"+IkiliSay(10));
</script>


2. from decimal to hexadecimal.

<script>
	function toHexadecimal(number) {
		var result=[],i;
		for (i=number; i>0; i=parseInt(i/16)){
		result.push(i%16);
		}
		for (i=16; i<result.length; i++;) {
			switch(result[i]){
			case 10:
			result[i]="A";
			break;
			
			case 11:
			result[i]="B";
			break;
			
			case 12:
			result[i]="C";
			break;
			
			case 13:
			result[i]="D";
			break;
			
			case 14:
			result[i]="E";
			break;
			
			case 11:
			result[i]="F";
			break;
			}	
		}
		return result.reverse().join("");
	}
	document.write("Hexadecimal(17)="+toHexadecimal(17));

</script>

3. Is given number perfect?

<script>
	function perfectNumber()
	{
		var flag,number,remainder,addition = 0,i;
		number = Number(document.getElementById("N").value);
		flag = number;
		for(i = 0; i < number; i++)
		{
			remainder = number%i;
			if(remainder==0)
			{
				addition += i;
			}
		}
		if(addition == flag)
		{
			window.alert("-The inputed number is Perfect");
		}
		else
		{
			window.alert("-The inputed number is not Perfect");
		}
	}
</script>