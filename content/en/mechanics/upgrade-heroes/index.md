---
title: 'Upgrade Heroes'
description: 'Calculate how many shards are needed to upgrade your heroes'
---

<form id="upgrade-hero">
  To upgrade a
  <select id="hero-type" onchange="calculateHeroUpgrade()">
    <option>Legendary</option>
    <option>Mythic</option>
  </select>
  hero

  <div class="star-option star-option-current">
    <span>From current level </span>
    <input
      id="from"
      type="range"
      min="0"
      max="15"
      value="0"
      onchange="this.nextElementSibling.value=this.value;calculateHeroUpgrade()"
    />
    <input
      type="number"
      name="amountInput"
      min="0"
      max="15"
      value="0"
      onchange="this.previousElementSibling.value=this.value;calculateHeroUpgrade()"
    />
    {{% hero-stars level="0" %}}
  </div>
  <div class="star-option star-option-target">
    <span>To target level </span>
    <input
      id="to"
      type="range"
      min="0"
      max="15"
      value="0"
      onchange="this.nextElementSibling.value=this.value;calculateHeroUpgrade()"
    />
    <input
      type="number"
      name="amountInput"
      min="0"
      max="15"
      value="0"
      onchange="this.previousElementSibling.value=this.value;calculateHeroUpgrade()"
    />
    {{% hero-stars level="0" %}}
  </div>
  <span id="result"></span>
</form>

{{% upgrade-hero %}}

<table class="text-center">
  <thead>
    <tr>
      <td rowspan="2">Tier</td>
      <td rowspan="2">Lv</td>
      <td rowspan="2">Star</td>
      <td colspan="3">Shard cost</td>
    </tr>
    <tr>
      <td>Each step</td>
      <td>Each star</td>
      <td>Total</td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="16" class="text-vertical">LEGENDARY</td>
      <td>1</td>
      <td class="bg-star1">{{% hero-stars level="1" %}}</td>
      <td>1</td>
      <td>5</td>
      <td rowspan="5">50</td>
    </tr>
    <tr>
      <td>2</td>
      <td class="bg-star1">{{% hero-stars level="2" %}}</td>
      <td>1</td>
      <td>5</td>
    </tr>
    <tr>
      <td>3</td>
      <td class="bg-star1">{{% hero-stars level="3" %}}</td>
      <td>2</td>
      <td>10</td>
    </tr>
    <tr>
      <td>4</td>
      <td class="bg-star1">{{% hero-stars level="4" %}}</td>
      <td>2</td>
      <td>10</td>
    </tr>
    <tr>
      <td>5</td>
      <td class="bg-star1">{{% hero-stars level="5" %}}</td>
      <td>4</td>
      <td>20</td>
    </tr>
    <tr>
      <td>6</td>
      <td class="bg-star2">{{% hero-stars level="6" %}}</td>
      <td>6</td>
      <td>30</td>
      <td rowspan="5">150</td>
    </tr>
    <tr>
      <td>7</td>
      <td class="bg-star2">{{% hero-stars level="7" %}}</td>
      <td>4</td>
      <td>20</td>
    </tr>
    <tr>
      <td>8</td>
      <td class="bg-star2">{{% hero-stars level="8" %}}</td>
      <td>4</td>
      <td>20</td>
    </tr>
    <tr>
      <td>9</td>
      <td class="bg-star2">{{% hero-stars level="9" %}}</td>
      <td>8</td>
      <td>40</td>
    </tr>
    <tr>
      <td>10</td>
      <td class="bg-star2">{{% hero-stars level="10" %}}</td>
      <td>8</td>
      <td>40</td>
    </tr>
    <tr>
      <td>11</td>
      <td class="bg-star3">{{% hero-stars level="11" %}}</td>
      <td>16</td>
      <td>80</td>
      <td rowspan="5">300</td>
    </tr>
    <tr>
      <td>12</td>
      <td class="bg-star3">{{% hero-stars level="12" %}}</td>
      <td>4</td>
      <td>20</td>
    </tr>
    <tr>
      <td>13</td>
      <td class="bg-star3">{{% hero-stars level="13" %}}</td>
      <td>8</td>
      <td>40</td>
    </tr>
    <tr>
      <td>14</td>
      <td class="bg-star3">{{% hero-stars level="14" %}}</td>
      <td>16</td>
      <td>80</td>
    </tr>
    <tr>
      <td>15</td>
      <td class="bg-star3">{{% hero-stars level="15" %}}</td>
      <td>16</td>
      <td>80</td>
    </tr>
    <tr>
      <td colspan="4" class="text-right">Total</td>      
      <td>500</td>
    </tr>
  </tbody>
</table>

<table class="text-center">
  <thead>
    <tr>
      <td rowspan="2">Tier</td>
      <td rowspan="2">Lv</td>
      <td rowspan="2">Star</td>
      <td colspan="3">Shard cost</td>
    </tr>
    <tr>
      <td>Each step</td>
      <td>Each star</td>
      <td>Total</td>
    </tr>
  </thead>
  <tbody>
    <tr>      
      <td rowspan="16" class="text-vertical">Mythic</td>
      <td>1</td>
      <td class="bg-star1">{{% hero-stars level="1" %}}</td>
      <td>2</td>
      <td>10</td>
      <td rowspan="5">100</td>
    </tr>
    <tr>
      <td>2</td>
      <td class="bg-star1">{{% hero-stars level="2" %}}</td>
      <td>2</td>
      <td>10</td>
    </tr>
    <tr>
      <td>3</td>
      <td class="bg-star1">{{% hero-stars level="3" %}}</td>
      <td>4</td>
      <td>20</td>
    </tr>
    <tr>
      <td>4</td>
      <td class="bg-star1">{{% hero-stars level="4" %}}</td>
      <td>4</td>
      <td>20</td>
    </tr>
    <tr>
      <td>5</td>
      <td class="bg-star1">{{% hero-stars level="5" %}}</td>
      <td>8</td>
      <td>40</td>
    </tr>
    <tr>
      <td>6</td>
      <td class="bg-star2">{{% hero-stars level="6" %}}</td>
      <td>12</td>
      <td>60</td>
      <td rowspan="5">300</td>
    </tr>
    <tr>
      <td>7</td>
      <td class="bg-star2">{{% hero-stars level="7" %}}</td>
      <td>8</td>
      <td>40</td>
    </tr>
    <tr>
      <td>8</td>
      <td class="bg-star2">{{% hero-stars level="8" %}}</td>
      <td>8</td>
      <td>40</td>
    </tr>
    <tr>
      <td>9</td>
      <td class="bg-star2">{{% hero-stars level="9" %}}</td>
      <td>16</td>
      <td>80</td>
    </tr>
    <tr>
      <td>10</td>
      <td class="bg-star2">{{% hero-stars level="10" %}}</td>
      <td>16</td>
      <td>80</td>
    </tr>
    <tr>
      <td>11</td>
      <td class="bg-star3">{{% hero-stars level="11" %}}</td>
      <td>32</td>
      <td>160</td>
      <td rowspan="5">600</td>
    </tr>
    <tr>
      <td>12</td>
      <td class="bg-star3">{{% hero-stars level="12" %}}</td>
      <td>8</td>
      <td>40</td>
    </tr>
    <tr>
      <td>13</td>
      <td class="bg-star3">{{% hero-stars level="13" %}}</td>
      <td>16</td>
      <td>80</td>
    </tr>
    <tr>
      <td>14</td>
      <td class="bg-star3">{{% hero-stars level="14" %}}</td>
      <td>32</td>
      <td>160</td>
    </tr>
    <tr>
      <td>15</td>
      <td class="bg-star3">{{% hero-stars level="15" %}}</td>
      <td>32</td>
      <td>160</td>
    </tr>
    <tr>
      <td colspan="4" class="text-right">Total</td>   
      <td>1000</td>
    </tr>
  </tbody>
</table>
<!-- 
<table class="text-center">
  <thead>
    <tr>
      <td rowspan="2">Tier</td>
      <td rowspan="2">Lv</td>
      <td rowspan="2">Star</td>
      <td colspan="3">Shard cost</td>
    </tr>
    <tr>
      <td>Each step</td>
      <td>Each star</td>
      <td>Total</td>
    </tr>
  </thead>
  <tbody>
    <tr>      
      <td rowspan="16" class="text-vertical">Epic</td>
      <td>1</td>
      <td class="bg-star1">{{% hero-stars level="1" %}}</td>
      <td>1</td>
      <td>5</td>
      <td rowspan="5">100</td>
    </tr>
    <tr>
      <td>2</td>
      <td class="bg-star1">{{% hero-stars level="2" %}}</td>
      <td>1</td>
      <td>5</td>
    </tr>
    <tr>
      <td>3</td>
      <td class="bg-star1">{{% hero-stars level="3" %}}</td>
      <td>2</td>
      <td>10</td>
    </tr>
    <tr>
      <td>4</td>
      <td class="bg-star1">{{% hero-stars level="4" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>5</td>
      <td class="bg-star1">{{% hero-stars level="5" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>6</td>
      <td class="bg-star2">{{% hero-stars level="6" %}}</td>
      <td></td>
      <td></td>
      <td rowspan="5"></td>
    </tr>
    <tr>
      <td>7</td>
      <td class="bg-star2">{{% hero-stars level="7" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>8</td>
      <td class="bg-star2">{{% hero-stars level="8" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>9</td>
      <td class="bg-star2">{{% hero-stars level="9" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>10</td>
      <td class="bg-star2">{{% hero-stars level="10" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>11</td>
      <td class="bg-star3">{{% hero-stars level="11" %}}</td>
      <td>32</td>
      <td>160</td>
      <td rowspan="5">600</td>
    </tr>
    <tr>
      <td>12</td>
      <td class="bg-star3">{{% hero-stars level="12" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>13</td>
      <td class="bg-star3">{{% hero-stars level="13" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>14</td>
      <td class="bg-star3">{{% hero-stars level="14" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>15</td>
      <td class="bg-star3">{{% hero-stars level="15" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td colspan="4" class="text-right">Total</td>   
      <td></td>
    </tr>
  </tbody>
</table>
-->
<!--
<table class="text-center">
  <thead>
    <tr>
      <td rowspan="2">Tier</td>
      <td rowspan="2">Lv</td>
      <td rowspan="2">Star</td>
      <td colspan="3">Shard cost</td>
    </tr>
    <tr>
      <td>Each step</td>
      <td>Each star</td>
      <td>Total</td>
    </tr>
  </thead>
  <tbody>
    <tr>      
      <td rowspan="16" class="text-vertical">Rare</td>
      <td>1</td>
      <td class="bg-star1">{{% hero-stars level="1" %}}</td>
      <td>1</td>
      <td>5</td>
      <td rowspan="5">100</td>
    </tr>
    <tr>
      <td>2</td>
      <td class="bg-star1">{{% hero-stars level="2" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>3</td>
      <td class="bg-star1">{{% hero-stars level="3" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>4</td>
      <td class="bg-star1">{{% hero-stars level="4" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>5</td>
      <td class="bg-star1">{{% hero-stars level="5" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>6</td>
      <td class="bg-star2">{{% hero-stars level="6" %}}</td>
      <td></td>
      <td></td>
      <td rowspan="5"></td>
    </tr>
    <tr>
      <td>7</td>
      <td class="bg-star2">{{% hero-stars level="7" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>8</td>
      <td class="bg-star2">{{% hero-stars level="8" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>9</td>
      <td class="bg-star2">{{% hero-stars level="9" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>10</td>
      <td class="bg-star2">{{% hero-stars level="10" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>11</td>
      <td class="bg-star3">{{% hero-stars level="11" %}}</td>
      <td></td>
      <td></td>
      <td rowspan="5"></td>
    </tr>
    <tr>
      <td>12</td>
      <td class="bg-star3">{{% hero-stars level="12" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>13</td>
      <td class="bg-star3">{{% hero-stars level="13" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>14</td>
      <td class="bg-star3">{{% hero-stars level="14" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>15</td>
      <td class="bg-star3">{{% hero-stars level="15" %}}</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td colspan="4" class="text-right">Total</td>   
      <td></td>
    </tr>
  </tbody>
</table> 
-->

Inspired by https://tophero.us/shard-calculator.html