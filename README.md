

				<label>Adultos:</label>
				<input type="number" id="adultomayorprecio" >
				<br><br>

				<label>Niños:</label>
				<input type="number" id="niñosprecio" >

<br><br>		<label>Mayores de edad:</label >
				<input type="number" id="adultomayorprecio" ><br>
<br><br>
					<label>Salida</label>
				<input type="date" id="salida" required>
<br><br>
 </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Total</td>
      <td id="preciototal"></td>
    </tr>
  </tfoot>
</table>

<button id="ResultButton">resultado</button>
<div id="result"></div>
		</div>
	<script>	
 const adultoprecio = 100; 
document.getElementById('adultoPrecio').innerText = `$${adultoprecio}`;

const niñosprecio = adultoprecio * 0.5;
document.getElementById('niñosprecio').innerText = `$${niñosprecio}`;

const adultomayorprecio = adultoprecio * 0.75;
document.getElementById('seniorPrice').innerText = `$${adultomayorprecio}`;

const totalPrice = adultoprecio + niñosprecio + adultomayorprecio;
document.getElementById('preciototal').innerText = `$${precio total}`;

const destination = 'TUA'; 
let ivaPercentage = 8;
if (destination !== 'AICM') {
  ivaPercentage = 16;
}
const resultDiv = document.getElementById('result');
const resultText = `IVA: ${ivaPercentage}%<br>Total con IVA: $${(preciototal * (1 + ivaPercentage / 100)).toFixed(2)}`;
resultDiv.innerHTML = resultText;



</script>
