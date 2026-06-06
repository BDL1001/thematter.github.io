---
title: PID Coefficients
subtitle: Tables (Circular, Frequency Sweep, etc.) 
image:
alt: 

caption:
  title: PID Control
  subtitle: Explanation & Values
  thumbnail: assets/img/portfolio/PID_Control_Thumbnail.png
---

<style>
caption {
  text-align: center;
  caption-side: top;
}
  
table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width: 100%;
}

td, th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
}

tr:nth-child(even) {
  background-color: #dddddd;
}
</style>

<b>Preset, optimal PID values were determined on all tracks through pre-race testing. Tuning potentiometers are adjusted until the ESP32 serial monitor's output matches these predetermined values for the respective tracks.<b>
<table>
  <caption>
    Drag Race
  </caption>
  <tr>
    <th><b>Nominal Speed</b></th>
    <th><b>Speed Increase</b></th>
    <th><b>Proportional Gain</b></th>
    <th><b>Integral Gain</b></th>
    <th><b>Derivative Gain</b></th>
  </tr>
  <tr>
    <td>200</td>
    <td>100</td>
    <td>90</td>
    <td>0.03</td>
    <td>0.56</td>
  </tr>
</table>

The nominal speed and speed increase were set much higher than other tracks due to the drag race's shape. As it is a track with minimal turns and bends and has a shape most similar to a straight track. The derivative gain is turned up to a significantly higher value than the other two tracks. This is to reduce as much overshoot and settling time as possible as traversing through the track in the least amount of time is the main priority. 
<br>
<br>

<table>
  <caption>
    Soft Circle (Loop)
  </caption>
  <tr>
    <th><b>Nominal Speed</b></th>
    <th><b>Speed Increase</b></th>
    <th><b>Proportional Gain</b></th>
    <th><b>Integral Gain</b></th>
    <th><b>Derivative Gain</b></th>
  </tr>
  <tr>
    <td>150</td>
    <td>100</td>
    <td>100.50</td>
    <td>0.03</td>
    <td>0.14</td>
  </tr>
</table>

The soft circle PID values were determined to sit in between the drag race and the frequency race as the track is essentially one continual turn. Not too straight, not too abrupt. For instance, whilst the speed increase is kept at a 100 similar to the drag race, the nominal speed should be reduced down to 150. 
<br>
<br>

<table>
  <caption>
    Frequency Sweep
  </caption>
  <tr>
    <th><b>Nominal Speed</b></th>
    <th><b>Speed Increase</b></th>
    <th><b>Proportional Gain</b></th>
    <th><b>Integral Gain</b></th>
    <th><b>Derivative Gain</b></th>
  </tr>
  <tr>
    <td>150</td>
    <td>0</td>
    <td>84</td>
    <td>0.01</td>
    <td>0.35</td>
  </tr>
</table>
The frequency sweep track, due to its sharp and unpredictable turns, had a nominal speed of only 150 rather than 200. The speed increase was also turned all the way down to 0 as the ability to traverse the track itself was more important than time. Both the proportional gain and integral gain were turned down to reduce overshoot that could prevent robot recovery during such sharp turns. While the derivative gain is turned up to a moderate value of 0.35 to anticipate these rapid track changes.
