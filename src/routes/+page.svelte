<script lang="ts">
	import { onMount } from 'svelte';
  import Logo from '$components/Logo.svelte';
  import Lung from '$components/Lung.svelte';
  import Bunny from '$components/Bunny.svelte';
  import CCLogo from '$components/CCLogo.svelte';
  import SCLLogo from '$components/SCLLogo.svelte';
  import Plurality from '$components/Plurality.svelte';
  import Specialists from '$components/Specialists.svelte';
  import { inview } from 'svelte-inview';
  import type { ObserverEventDetails, ScrollDirection, Options } from 'svelte-inview';
  let showheader: boolean;

  let isInView: boolean;
  let scrollDirection: ScrollDirection;
  const puffoptions: Options = {
    rootMargin: '-50px',
    unobserveOnEnter: false,
  };

  const handleChange = ({ detail }: CustomEvent<ObserverEventDetails>) => {
    isInView = detail.inView;
    scrollDirection = detail.scrollDirection.vertical;
  };

  let headertext = '';
  let headercolor = '';
  const options = {threshold: '.1'};
  const sectionoptions = {threshold: '.3'};  

</script>

<header class="showheader" class:showheader>
  <a
  class="logo"
  aria-label="Menu"
  href=''
  rel="noopener noreferrer"
  >

  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 235 235">
  <g class="logo-1">
    <g id="Layer_1" data-name="Layer 1">
      <g>
        <g>
          <circle cx="117.1" cy="80.62" r="4.24"/>
          <circle cx="119.86" cy="56.58" r="5.66"/>
          <circle cx="127.58" cy="32.53" r="7.07"/>
          <circle cx="139.17" cy="8.49" r="8.49"/>
        </g>
        <g>
          <circle cx="98.72" cy="85.76" r="4.24"/>
          <circle cx="89.08" cy="63.56" r="5.66"/>
          <circle cx="83.75" cy="38.87" r="7.07"/>
          <circle cx="81.76" cy="12.26" r="8.49"/>
        </g>
        <g>
          <circle cx="85.37" cy="99.41" r="4.24"/>
          <circle cx="65.92" cy="84.99" r="5.66"/>
          <circle cx="48.96" cy="66.28" r="7.07"/>
          <circle cx="33.93" cy="44.23" r="8.49"/>
        </g>
        <g>
          <circle cx="80.62" cy="117.9" r="4.24"/>
          <circle cx="56.58" cy="115.14" r="5.66"/>
          <circle cx="32.53" cy="107.42" r="7.07"/>
          <circle cx="8.49" cy="95.83" r="8.49"/>
        </g>
        <g>
          <circle cx="85.76" cy="136.28" r="4.24"/>
          <circle cx="63.56" cy="145.92" r="5.66"/>
          <circle cx="38.87" cy="151.25" r="7.07"/>
          <circle cx="12.26" cy="153.24" r="8.49"/>
        </g>
        <g>
          <circle cx="99.41" cy="149.63" r="4.24"/>
          <circle cx="84.99" cy="169.08" r="5.66"/>
          <circle cx="66.28" cy="186.04" r="7.07"/>
          <circle cx="44.23" cy="201.07" r="8.49"/>
        </g>
        <g>
          <circle cx="117.9" cy="154.38" r="4.24"/>
          <circle cx="115.14" cy="178.42" r="5.66"/>
          <circle cx="107.42" cy="202.47" r="7.07"/>
          <circle cx="95.83" cy="226.51" r="8.49"/>
        </g>
        <g>
          <circle cx="136.28" cy="149.24" r="4.24"/>
          <circle cx="145.92" cy="171.44" r="5.66"/>
          <circle cx="151.25" cy="196.13" r="7.07"/>
          <circle cx="153.24" cy="222.74" r="8.49"/>
        </g>
        <g>
          <circle cx="149.63" cy="135.59" r="4.24"/>
          <circle cx="169.08" cy="150.01" r="5.66"/>
          <circle cx="186.04" cy="168.72" r="7.07"/>
          <circle cx="201.07" cy="190.77" r="8.49"/>
        </g>
        <g>
          <circle cx="154.38" cy="117.1" r="4.24"/>
          <circle cx="178.42" cy="119.86" r="5.66"/>
          <circle cx="202.47" cy="127.58" r="7.07"/>
          <circle cx="226.51" cy="139.17" r="8.49"/>
        </g>
        <g>
          <circle cx="149.24" cy="98.72" r="4.24"/>
          <circle cx="171.44" cy="89.08" r="5.66"/>
          <circle cx="196.13" cy="83.75" r="7.07"/>
          <circle cx="222.74" cy="81.76" r="8.49"/>
        </g>
        <g>
          <circle cx="135.59" cy="85.37" r="4.24"/>
          <circle cx="150.01" cy="65.92" r="5.66"/>
          <circle cx="168.72" cy="48.96" r="7.07"/>
          <circle cx="190.77" cy="33.93" r="8.49"/>
        </g>
        <g>
          <g>
            <circle cx="104.74" cy="69.89" r="4.24"/>
            <circle cx="103.85" cy="45.24" r="5.66"/>
            <circle cx="108.28" cy="19.16" r="7.07"/>
          </g>
          <g>
            <circle cx="82.65" cy="82.65" r="4.24"/>
            <circle cx="69.55" cy="61.75" r="5.66"/>
            <circle cx="60.34" cy="36.94" r="7.07"/>
          </g>
          <g>
            <circle cx="69.89" cy="104.74" r="4.24"/>
            <circle cx="48.09" cy="93.19" r="5.66"/>
            <circle cx="27.72" cy="76.31" r="7.07"/>
          </g>
          <g>
            <circle cx="69.89" cy="130.26" r="4.24"/>
            <circle cx="45.24" cy="131.15" r="5.66"/>
            <circle cx="19.16" cy="126.72" r="7.07"/>
          </g>
          <g>
            <circle cx="82.65" cy="152.35" r="4.24"/>
            <circle cx="61.75" cy="165.45" r="5.66"/>
            <circle cx="36.94" cy="174.66" r="7.07"/>
          </g>
          <g>
            <circle cx="104.74" cy="165.11" r="4.24"/>
            <circle cx="93.19" cy="186.91" r="5.66"/>
            <circle cx="76.31" cy="207.28" r="7.07"/>
          </g>
          <g>
            <circle cx="130.26" cy="165.11" r="4.24"/>
            <circle cx="131.15" cy="189.76" r="5.66"/>
            <circle cx="126.72" cy="215.84" r="7.07"/>
          </g>
          <g>
            <circle cx="152.35" cy="152.35" r="4.24"/>
            <circle cx="165.45" cy="173.25" r="5.66"/>
            <circle cx="174.66" cy="198.06" r="7.07"/>
          </g>
          <g>
            <circle cx="165.11" cy="130.26" r="4.24"/>
            <circle cx="186.91" cy="141.81" r="5.66"/>
            <circle cx="207.28" cy="158.69" r="7.07"/>
          </g>
          <g>
            <circle cx="165.11" cy="104.74" r="4.24"/>
            <circle cx="189.76" cy="103.85" r="5.66"/>
            <circle cx="215.84" cy="108.28" r="7.07"/>
          </g>
          <g>
            <circle cx="152.35" cy="82.65" r="4.24"/>
            <circle cx="173.25" cy="69.55" r="5.66"/>
            <circle cx="198.06" cy="60.34" r="7.07"/>
          </g>
          <g>
            <circle cx="130.26" cy="69.89" r="4.24"/>
            <circle cx="141.81" cy="48.09" r="5.66"/>
            <circle cx="158.69" cy="27.72" r="7.07"/>
          </g>
        </g>
        <circle class="logo-2" fill="{headercolor}" cx="117.5" cy="117.5" r="26.68"/>
      </g>
    </g>
  </g>
</svg>

	</a>
  <h3>{headertext}</h3>
</header>

<section 
	use:inview={options}
	class="banner-section"
    on:inview_change={(event) => {
      const { inView } = event.detail;
      showheader = inView;
    }}
>
	<div class="head">
			<div class="puff-holder" use:inview={puffoptions} on:inview_change={handleChange}>
				<div
      class:animate={isInView}
      class:goingin={scrollDirection === 'down'}
      class:goingout={scrollDirection === 'up'}>
				<Logo />
			</div>
			</div>
			<h1>Breathe,<br /> Allentown.</h1>
	</div>
</section>

<section
class="introduction"
use:inview={sectionoptions}
on:inview_enter={(event) => {
      headertext = 'Introduction';
      headercolor = 'var(--black-color)';
    }}
>

	<div class="grid standard-padding">

		<div class="width-12-12-m width-6-12-i width-6-12 order-2 intro-text">
			<h3>Let's Not Be Number 1</h3>
			<p class="lede">The Lehigh Valley has been referred to as the number one asthma capital of the United States. There are a number of conditions that can make a community vulnerable to chronic disease. Inadequate access to care, infrastructural issues, environment, biology, behavior, and systemic injustice all contribute. These issues are not insurmountable. 

			<p>Enacted in 1963 and subsequently updated in 1990, the <a href="https://www.epa.gov/laws-regulations/summary-clean-air-act" target="_blank">Clean Air Act</a> has proven to be a great success in improving air quality in the United States that serves as an example pointing to the efficacy of interventions. But what else can be done here in the Lehigh Valley?</p>
			
			<p>Community, individual, and policy level efforts that seek to address air quality, personal health, living environments and systemic injustice can all contribute to lowering the incidence of chronic respiratory health issues such as asthma. Let's explore. 
		</div>

		<div class="width-12-12-m width-6-12-i width-6-12 order-1 intro-graphic">
			<Lung />
		</div>

	</div>

</section>


<section
class="smoking-holder"
use:inview={sectionoptions}
on:inview_enter={(event) => {
      headertext = 'Personal Health';
      headercolor = 'var(--red-color)';
    }}
>

<div class="smoking">
	<div class="shout">
		<h2>17%</h2>
		<p>of the adult population<br> regularly smokes or vapes.
	</div>
</div>

<div class="grid standard-padding no-gutter">
	<div class="width-12-12-m width-12-12-i width-12-12">
	<h3>Risk Factor: Tobacco Use</h3>
			<div class="two-column-text">
			<p class="lede">Tobacco is one of the main risk factors for chronic respiratory disease. Here in the Lehigh Valley an estimated 17% of the population regularly smokes or vapes. This is a bit higher than the 13% average of the United States. 

			<p>Smoking is unhealthy for everyone, but it is especially harmful for people with asthma. In fact, smoking is one of the most common asthma triggers. If someone ends up in the emergency room due to an asthma attack, there's a good chance that they have been smoking or vaping. In fact, here in the Lehigh Valley, 1 out of 3 ER visits include some element of issues connected to respiratory health.</p>

			<p>Tobacco smoke introduces thousands of harmful chemicals into the lungs, many of which are irritants. For people with asthma, these substances inflame airways and increase mucus production. This can cause symptoms of coughing, wheezing and shortness of breath. It can trigger more frequent and severe asthma attacks. Smoking also weakens the capacity of lungs to do their job over time, making it harder for people to manage their symptoms effectively.</p>

			<p>Some smokers have turned to vaping to help them quit. However, there is now a growing body of research suggesting that vaping is also harmful to lung health. Vaping is a relatively new technology and scientists are still researching how safe it is to human health. More studies are beginning to show that vaping can increase inflammation in the airways and can cause breathing difficulties which intensify asthma symptoms and trigger asthma attacks.</p>

			<p>Avoiding tobacco products before it comes a problem is one way to address this issue. Workplace rules and public policy contributes to helping people stay away from tobacco. Making moves as an individual to quit the use of tobacco products is another way forward. Easier said than done, but it can be done –and <a href="https://www.lvhn.org/medical-services/tobacco-treatment-program" target="_blank">help</a> is <a href="https://www.slhn.org/wellnow/substance-misuse/tobacco-cessation-program" target="_blank">available</a>.</p>
			
		</div>

		</div>
</div>

</section>


<section
class="healthcare-holder"
use:inview={sectionoptions}
on:inview_enter={(event) => {
      headertext = 'Healthcare';
      headercolor = 'var(--red-color)';
    }}
>

<div class="specialists-wrap">
	<div class="specialists">
		<div class="specialist-inner">
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Plurality />
			</div>
			<div class="tile">
				<Specialists />
			</div>
		</div>
	</div>
	<div class="spec-label">
		In the Allentown, Bethlehem, and Easton metro area, there is only one specialist for every 100,000 patients. 
	</div>
</div>

	<div class="grid standard-padding no-gutter">
	<div class="width-12-12-m width-12-12-i width-12-12">
	<h3>Risk Factor: Access to Specialitsts</h3>
			<div class="two-column-text">
				<p class="lede">Living in an area where there are fewer specialists is frustrating for those who need care. Booking appointments months in advance, traveling long distances, and giving up altogether are common. Lack of access, and needing to take time in order to travel when appointments become available is a burden on personal finances and time, especially when frequent trips are needed, and especially when any additional costs can rock the balance of the household.</p>

				<p>Successful management of chronic respiratory health issues requires a team effort between the patient
				and their health care providers. Someone with persistent asthma should be in the care of a specialist. Pulmonologists, allergists, and immunologists can provide specialized care for people with asthma and may have more experience treating patients with severe asthma or allergic asthma than a primary care physician.</p>
				
				<p>Access to appropriate medical care is dependent upon different factors, including socioeconomic
				status and insurance status. The lack of availability of nearby asthma specialists leads to poor asthma outcomes.</p>

				<p>What can be done? Finding ways to bring care to the neighborhoods that need it is one way forward. Care teams that visit community centers, schools, assisted living facilities can help. Additionally, addressing sytemic healthcare issues is hugely important –and takes courage at every level.</p>
			</div>

		</div>
</div>

</section>


<section
class="environment-holder"
use:inview={sectionoptions}
on:inview_enter={(event) => {
      headertext = 'Living Environment';
      headercolor = 'var(--green-color)';
    }}
>

<div class="environment">
	<div class="shout">
		<h2>43%</h2>
		<p>of housing has issues that<br> contribute to poor health.
	</div>
</div>
<div class="citation">Bethlehem and South Bethlehem, Pa. Looking North East. <a target="_blank" href="https://www.loc.gov/item/98508515/">Schwartz & Weaver, c1877</a>.</div>

<div class="grid standard-padding no-gutter">
	<div class="width-12-12-m width-12-12-i width-12-12">
	<h3>Risk Factor: Housing Concerns</h3>
			<div class="two-column-text">
			<p class="lede">Much of the housing stock in the Allentown, Bethlehem and Easton metro area was developed for factory worker families of the early to mid 20th century. While it can be said that many of these houses were constructed with a pride of craft and longevity in mind, there are concerns related to old infrastructure. Leaks, poor or dirty ventilation, peeling paint, clunky old furnaces, and overdue maintenance all contribute to poor living conditions.</p>

			<p>As houses age, insulation settles, leaks develop, and hidden spaces become susceptible to mold. For people with chronic conditions, triggers and allergens in the home (such as dust, pests, and mold) can cause asthma and allergy symptoms. Remediation and renovation is expensive work. For many, perhaps the best course of action is to address issues as they occur in rooms most used.</p>

			<p>
				What else can be done? Laws that encourage landlords to address housing issues that impact health is one way forward. Programs that aid and incentivize property owners to make much needed repairs is another. Improving the living environment of the places we inhabit is doable. It's worth looking to examples like the <a href="https://www.dchealthyhousingcollaborative.org/" target="_blank">DC Healthy Housing Collaborative (DCHHS)</a>, and the <a href="https://www.phi.org/thought-leadership/a-path-forward-sustainable-financing-for-asthma-education-and-home-environmental-trigger-remediation-in-california/" target="_blank">California Asthma Financing Workgroup</a>.
			</p>
			
		</div>

		</div>
</div>

</section>

<section
class="air-holder"
use:inview={sectionoptions}
on:inview_enter={(event) => {
      headertext = 'Air Quality';
      headercolor = 'var(--blue-color)';
    }}
>

<div class="air">
		<img src="/img/particle-scale.png" />
		<div class="ns">
			<iframe
			  id="inlineFrameExample"
			  title="Inline Frame Example"
			  width="120%"
			  height="120%"
			  src="https://earth.nullschool.net/#current/particulates/surface/level/overlay=pm2.5/orthographic=-78.05,39.02,5179">
			</iframe>
		</div>
</div>
<div class="citation">Wind + Particulate Matter &lt; 2.5µm @ surface. <a target="_blank" href="https://earth.nullschool.net/">earth.nullschool.net</a>.</div>

<div class="grid standard-padding no-gutter">
	<div class="width-12-12-m width-12-12-i width-12-12">
	<h3>Risk Factor: Air Quality</h3>
			<div class="two-column-text">
			<p class="lede">If you grew up in the Lehigh Valley before the 1970's you might remember soot on your windowsill from the prevalent use of coal in the region. Times have changed and today coal is no longer the preferred choice of energy. While air pollution is no longer as visible, or tactile, as it once was, it does not mean we are in the clear.</p>

			<p>An averagre of 50 days out of the year in the Allentown region are considered "Unhealthy for Sensitive Groups" by the <a href="https://www.airnow.gov/aqi/aqi-basics/" target="_blank">EPA Air Quality Index</a>. This is largely due to high levels of 2.5µm particluate matter related to vehicle emissions that tends to swirl about the valley when certain meteorological conditions arise. Unhealthy air quality is a contributor to poor respiratory health and on really bad days can trigger an episode amongst those who suffer the most.</p>

			<p>What can be done? Incentives that encourage the use of and investment in public transport, strengthening and enforcement of laws prohibiting idling vehicles, and encouraging the adoption of electric vehicles and other forms of alternative transporation are all proven to reduce the amount of emmisions related particulates. </p>

			<p>Additionally, investment in more robust trails and paths for cyclists and walkers would be a double win for health and air. Lastly, and though it may sound far-fetched (the technology is just around the corner): municipal scale air purification systems could be installed in the built environment of areas with consistently high levels of particulate material.</p>
		</div>

		</div>
</div>

</section>

<div id="footer" class="standard-padding">
    <div class="grid">

    	<div class="width-12-12-m width-6-12-i width-6-12">
      	<p>
            <a
              aria-label="Creative Commons"
              target="_blank"
              href="/"
              rel="noopener noreferrer"
              > <CCLogo /></a> 2025 Kevin Lahoda. </p>

              <p>Allentown Breathes is a exploratory project investigating inquiry based design for environmental and public health.
          </p>
        <p>Be in touch. klahoda@gmail.com</p>
      </div>

      <div class="width-12-12-m width-6-12-i width-6-12">

        <div class="stuff">
            <a href="https://kevinlahoda.com/" target="_blank" title="Kevin Lahoda">
            <Bunny />
            </a>
            
            <a href="https://smallcitieslab.org/" target="_blank" title="Small Cities Lab">
            <SCLLogo />
            </a>
        </div>

      </div>

    </div>
</div>

<style>

header {
	position: fixed;
	z-index: 999999999;
	top: 0;
	left: 0;
	width: 100%;
	padding: 1rem;
	background-color: var(--light-grey-color);
	transition: all .5s cubic-bezier(.215,.61,.355,1);
	display: flex;
  justify-content: flex-end;
  align-items: center;
	}

header h3 {
	font-weight: 600;
	margin: 0;
}

header.showheader {
  	opacity: 0;
}

header a {
	margin-right: auto;
	display: block;
	width: 2rem;
	height: 2rem;
}

.banner-section {
  aspect-ratio: 1;
  overflow: hidden;
  background-image: url('/img/a-map.jpg');
  background-size:cover;
  background-position: center;
  padding: 3em;
  display: flex;
  align-items: center;
}

.head {
	padding-top: 7em;
	position: relative;
}

.puff-holder {
	position: absolute;
	top: 0;
	right: 0;
	width: 8em;
	height: auto;
}

.puff-holder div {
	transition: all 1s ease-in-out;
}

.goingout {
	opacity: 0;
	transform: scale(50) rotate(180deg);
}

.goingout svg {
	display: none;
}

section h3 {
  font-weight: 500;
  font-size: 1.5em;
  margin-bottom: 1.4rem;
}

.banner-section h1 {
  display: inline !important;
  line-height: 1em;
  font-size: 4em;
}

p.lede {
	font-weight: 500;
}

.introduction .intro-graphic {
	align-content: center;
}

.introduction .intro-graphic svg {
  max-width: fit-content;
  margin-inline: auto;
}

.smoking-holder {
	
}

.smoking {
	background-color: var(--red-color);
	background-image: url('/img/vaping-smoke.jpg');
  background-size:cover;
  background-position: center;
	width: 100vw;
	aspect-ratio: 1;
	align-content: center;
}

.shout {
	text-align: left;
	max-width: fit-content;
  margin-inline: auto;
  color: var(--light-grey-color);
  font-weight: 500;
  border: 2px solid var(--light-grey-color);
  display: flex;
}

.shout h2 {
	padding: 1rem;
	font-size: 3em;
	line-height: .85em;
	margin-bottom: 0;
	font-weight: 500;
	border-right: 2px solid var(--light-grey-color);
}

.shout p {
	font-size: 1em;
	padding: 1rem;
}

.specialists-wrap {
	background-color: var(--red-color);
	padding: 2vw;
}

.specialists {
	align-content: center;
}

.specialist-inner {
	display: grid;
  grid-template-columns: repeat(5, 1fr);
	grid-gap: 2vw;
	width: calc(100vw - 4vw);
}

.spec-label {
	margin-top: 1em;
	margin-left: .5em;
	font-weight: 500;
}

.tile {
}

.environment-holder {
	
}

.environment {
	background-image: url('/img/bethlehem-view.jpg');
  background-size:cover;
  background-position: center;
	width: 100vw;
	aspect-ratio: 1;
	align-content: center;
}


.tile svg {
	max-width: fit-content;
  margin-inline: auto;
}

.air-holder {
	
}

.air {
	width: 100vw;
	aspect-ratio: 1;
	align-content: center;
	position: relative;
}

.air img {  
	width: 100%;
	height: auto;      
  display:block;
  margin-left:auto;
  margin-right:auto;
}

.air .ns {
	position: absolute;
	top: 0;
	left: 0;
	z-index: -1;
	width: 100%;
	height: 100%;
	background-color: var(--blue-color);
	overflow: hidden;
}

.air .ns iframe {
	margin-top: -2px;
	margin-left: -2px;
	mix-blend-mode: overlay;
	filter: grayscale(80%);
	opacity: .6;
}

.citation {
	color: var(--black-color);
	background-color: var(--lighter-grey-color);
	text-align: right;
	font-size: .75em;
	padding: .25em .5em;
}

.citation a {
	color: var(--black-color);
}
.citation a:hover {
	text-decoration: none;
}

  #footer {
    margin-top: auto;
    font-size: 0.85em;
    overflow: hidden;
    background: var(--light-grey-color);
    color: var(--black-color);
    letter-spacing: 1px;
  }

  #footer ::selection {
    color: var(--lighter-grey-color);
    background: var(--black-color);
  }

  #footer p:first-child {
    margin-top: 0;
  }

  #footer p:last-child {
    margin-bottom: 0;
  }

  #footer a {
    color: var(--black-color);
    text-decoration: none;
    transition: 0.3s;
  }

  #footer a:hover {
    color: var(--grey-color);
  }

  #footer .stuff {
  	height: 100%;
    display: flex;
    justify-content: flex-start;
    align-items: flex-end;
  }

  #footer .stuff a {
    margin-right: 2em;
  }


@media (min-width: 48rem) {

	.banner-section {
		aspect-ratio: auto;
  	height: 100vh;
	}

	.smoking, .environment, .air {
	aspect-ratio: auto;
	height: calc(100vh - 3rem);
}

	.two-column-text {
		column-count: 2;
		column-gap: 4vw;
	}

	.shout h2 {
		padding: .75rem 1rem 1rem 1rem;
		font-size: 4em;
	}

	.shout p {
		font-size: 1.25em;
		padding: .75rem 1rem 1rem 1rem;
	}

	.air img {  
		height: 100%;
		width: auto;      
	}

	header a {
	width: 3rem;
	height: 3rem;
}

}

@media (min-width: 48rem) and (max-width: 79.99rem) {
	.banner-section h1 {
  		font-size: 6em;
	}
}

@media (min-width: 80rem) {
	.banner-section h1 {
  		font-size: 6em;
	}
	header a {
	width: 4rem;
	height: 4rem;
}
}

</style>