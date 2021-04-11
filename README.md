# Variable_DC_Power_Supply
<!-- wp:paragraph -->
<p><strong>Project Statement</strong><br>Design and simulate a variable power supply which takes an AC input of 230V rms at 50 Hz and gives a DC output that can vary in the range of 0-30V and maximum output load current should be 1-1.5A.<br>In this project we will design a Transformer Based Linear Convert to convert 230 rms AC to 0-30V DC with max load current of 1 – 1.5A.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><br><strong>Components Required</strong><br>• 230 rms AC voltage source<br>• Transformer (230 rms to 36V)<br>• Diodes<br>• Capacitors<br>• Resistors<br>• Potentiometer<br>• LM317S (1.5A Adjustable Output Positive Voltage Regulator)<br>Circuit Diagram<br>First, we will design a block diagram of above-mentioned project statement.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":155,"width":491,"height":171,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><img src="https://electronicinstruction.files.wordpress.com/2021/04/power_supply_block_diagram.jpg?w=636" alt="" class="wp-image-155" width="491" height="171"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><strong>Design Explanation</strong><br>Firstly, the AC input (230V rms) given to the transformer. Transformer convert the 230V rms to 36V AC. Then the Full Wave rectifier convert the 36V AC to 36V DC pulsating DC. This ripple of voltage is compensated by the filter that converts that DC signal to smoother DC signal. Next to filter we use LM317S voltage regulator that regulate the signal and make it more smoother means remove more ripples.Transformer We use step-down transformer in the design. A step-down transformer is a type of transformer, which converts high voltage at primary side to low voltage at the secondary side. If we speak in terms of coil winding, the primary winding of step-down transformer has more turn than the AC Transformer Full Wave Rectifier Filter LM317S Regulator circuit Protection Circuit Load<br>secondary winding. In this project, we step down the 230V rms to 36V DC. As we use<br>Proteus for the simulation so, it takes primary and secondary inductance as input to<br>convert the voltage. So, we have calculated inductance ratio by using formula given in design calculation section. We take 81H as primary inductance and 1H as secondary inductance.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Full Wave Bridge Rectifier</strong><br>Next to transformer there is a full wave bridge rectifier is connected. It uses four diodes connect in a way like Wheatstone bridge<br>The four diodes labelled D1 to D4 are arranged in “series pairs” with only two diodes conducting current during each half cycle.<br>• <strong>The Positive Half-cycle</strong><br>During the positive half cycle of the supply, diodes D1 and D2 conduct in series while<br>diodes D3 and D4 are reverse biased.<br>• <strong>The Negative Half-cycle</strong><br>During the negative half cycle of the supply, diodes D3 and D4 conduct in series, but<br>diodes D1 and D2 switch “OFF” as they are now reverse biased.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Filter for Pulsating DC</strong><br>After Bridge rectifier, we use filter for pulsating DC that remove the ripple from the DC signal and make it smoother. If we use capacitor of low value then the DC signal not fully smooth there is a ripple in it. And if we use capacitor of high value then the load current may not be the same as we want. So, we use capacitor of 4700uF and 1mF capacitor in parallel that make the signal smooth.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><br><strong>LM317S Voltage Regulator</strong><br>LM317 is used for the voltage regulation. LM317 is a monolithic positive voltage regulator IC. Being monolithic, all the components are inbuilt on the same semiconductor chip making the IC small in size having less power consumption and low cost. The IC has three pins – <br>1) Input pin where maximum 40 V DC can be supplied, <br>2) Output pin which provides output voltage in the range of 1.25 V to 37 V and <br>3) Adjust pin which is used to vary the output voltage corresponding to the applied input voltage. For input up to 40 V, the output can vary from 1.25 V to 37 V.<br>For setting the desired voltage at the output of LM317, resistive voltage divider circuit is used between the output pin and ground. By the effect of this configuration, the voltage at the output pin can be adjusted. The value of resistive voltage divider needs to be chosen in such a way that it can provide required voltage range at the output.<br>Our desired voltage output is 0-30V DC. As mentioned above use voltage divider with the<br>voltage regulator to get the desires output. In our design we use potentiometer in the place of one the resistor in voltage divider circuit that allows us to change voltage according to our requirement.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><br><strong>Short Circuit Protection</strong><br>A diode is connected between the voltage input and voltage output terminals of 317 IC so that it can prevent the external capacitor from discharging through the IC during an input short circuit. When the input is shorted then the cathode of the diode is at ground potential. The anode terminal of the diode is at high voltage since C2 is fully charged. Therefore, in such a case, the diode is forward biased and all the discharging current from capacitor passes through the diode to the ground. This saves the LM317 IC from the back current.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Circuit Simulations</strong><br>We use proteus for the simulation of variable DC power supply</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Circuit Diagram</strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":161,"width":665,"height":281,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><img src="https://electronicinstruction.files.wordpress.com/2021/04/circuit-diagram.jpg?w=620" alt="" class="wp-image-161" width="665" height="281"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>First, we design the block diagram of the circuit all parameter for the simulation is calculated.<br>Now we patched the circuit in Proteus for the simulation.<br>Vsine block generates the 230V rms that then converted to 36V AC using transformer</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Conclusion</strong><br>Now we compare the results and out requirement. We want to design a Dc variable power supply of 0 – 30V and load current with maximum limit of 1 – 1-.5A above mentioned waveforms showed that the minimum voltage we get is 1.25V and min current is about 63mA and the maximum current we achieve is around 1.4A and max voltage around 27V.<br>If we use the high value of capacitor for filtering then it is better but then we have to make<br>changes in our circuit to get the desired output because it reduces the output voltage.</p>
<!-- /wp:paragraph -->
