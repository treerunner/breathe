<script lang="ts">
	import { onMount } from 'svelte';
  import Logo from '$components/Logo.svelte';
  import Lung from '$components/Lung.svelte';
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
			<p class="lede">The Lehigh Valley has been referred to as the number one asthma capital of the United States. There are a number of conditions that can make a community vulnerable to chronic disease. Inadequate access to care, infrastructure, environment, biology, behavior, and systemic injustice all contribute. These issues are not insurmountable. 

			<p>Put into place in 1963, and subsequently updated in 1990, the Clean Air Act has proven to be a great success in improving air quality in the United States and serves as one example that points to the efficacy of interventions. But what more can be done here in the Lehigh Valley?</p>
			
			<p>Community, government, and individual efforts that seek to address air quality, personal health, living environments and systemic injustice can all contribute to lowering the incidence of chronic respiratory health issues such as asthma. Let's explore. 
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
	<div class="smoking-shout standard-padding">
		<h2>17%</h2>
		<p>of the adult population regular smokes or vapes.
	</div>
</div>

<div class="grid standard-padding no-gutter">
	<div class="width-12-12-m width-12-12-i width-12-12">
	<h3>Risk Factor: Tobacco Use</h3>
			<div class="two-column-text">
			<p class="lede">Tobacco is one of the main risk factors for chronic respiratory disease. Here in the Lehigh Valley an estimated 17% of the population regularly smokes or vapes. This is a significant jump from the 13% average of the United States. 

			<p>Smoking is unhealthy for everyone, but it is especially harmful for people with asthma. In fact, smoking is one of the most common asthma triggers. If someone ends up in the emergency room due to an asthma attack, there's a good chance that they have been smoking or vaping.</p>

			<p>Tobacco smoke introduces thousands of harmful chemicals into the lungs, many of which are irritants. For people with asthma, these substances worsen airway inflammation and increase mucus production. This can cause symptoms of coughing, wheezing and shortness of breath. It can trigger more frequent and severe asthma attacks. Smoking also weakens lung function over time, making it harder for people with asthma to manage their symptoms effectively.</p>

			<p>Some smokers have turned to vaping to help them quit. There is now a growing body of research suggesting that vaping is also harmful to lung health. However, vaping is a relatively new technology and scientists are still researching how safe it is to our health. More studies are beginning to show that vaping can increase inflammation in the airways and cause breathing difficulties which can intensify asthma symptoms and trigger asthma attacks.</p>

			<p>Avoiding tobacco products before it comes a problem is one way to address this issue. Workplace rules and public policy works to help people stay away from tobacco. Making moves as an individual to quit the use of tobacco products is another way forward. Easier said than done, but it can be done –and help is available.</p>
			
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
				<p class="lede">Living in an area where there are fewer specialists is frustrating for those who need care. Booking appointments months in advance, traveling long distances, and giving up altogether are common. Lack of access, and needing to take time in order to travel when appointments become available is a burden on personal finances and time, especially when frequent trips are needed, and especially when any additional cost rocks the balance of the household.</p>

				<p>Successful management of chronic respiratory health issues requires a team effort between the patient
				and their health care providers. Someone with persistent asthma might need to be in the care of a specialist. Pulmonologists, allergists, and immunologists, for example, can provide specialized care for people with asthma and may have more experience
				treating patients with severe asthma or allergic asthma than a primary care physician.</p>
				
				<p>Access to appropriate medical care is dependent upon different factors, including socioeconomic
				status and insurance status. The lack of availability of nearby asthma specialists leads to poor asthma outcomes.</p>

				<p>What can be done? Finding ways to bring care to the neighborhoods that need it is one way forward. Care teams that visit community centers, schools, assisted living facilities can help. Additionally, addressing healthcare infrastructure is hugely important and takes courage.</p>
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
	<div class="environment-shout standard-padding">
		<h2>43%</h2>
		<p>of housing has issues that contribute to poor health.
	</div>
</div>

<div class="grid standard-padding no-gutter">
	<div class="width-12-12-m width-12-12-i width-12-12">
	<h3>Risk Factor: Housing Concerns</h3>
			<div class="two-column-text">
			<p class="lede">Much of the housing stock in the Allentown, Bethlehem and Easton metro area was developed for factory worker families of the early to mid 20th century. While it can be said that many of these houses were constructed with a pride of craft and longevity in mind, there are concerns related to old infrastructure. Leaks, poor or dirty ventilation, peeling paint, clunky old furnaces and oil burners all contribute to poor living conditions.</p>

			<p>As houses age, insulation settles, and leaks develop, hidden spaces become susceptible to mold. For people with chronic conditions, triggers and allergens in the home (such as dust, pests, and mold) can cause asthma and allergy symptoms. Remediation and renovation is expensive work. For many, perhaps the best course of action is to address issues as they occur in rooms most used.</p>

			<p>
				What else can be done? Laws that encourage landlords to address housing issues that impact health is one way forward. Programs that aid and incentivize propoerty owners to make much needed repairs is another. Improving the living envirnonments of the places we inhabit is doable. It's worth looking to examples like the <a href="https://www.dchealthyhousingcollaborative.org/" target="_blank">DC Healthy Housing Collaborative (DCHHS)</a>, and the <a href="https://www.phi.org/thought-leadership/a-path-forward-sustainable-financing-for-asthma-education-and-home-environmental-trigger-remediation-in-california/" target="_blank">California Asthma Financing Workgroup</a>.
			</p>
			
		</div>

		</div>
</div>

</section>


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
  height: 100vh;
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
  font-size: 5em;
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
	height: calc(100vh - 3rem);
	align-content: center;
}

.smoking-shout {
	max-width: fit-content;
  margin-inline: auto;
  color: var(--light-grey-color);
  text-align: center;
  font-weight: 500;
}

.smoking-shout h2 {
	font-size: 10em;
	line-height: .85em;
	margin-bottom: .15em;
	font-weight: 500;
}

.smoking-shout p {
	font-size: 1.5em;
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
	background-color: var(--red-color);
	background-image: url('/img/bethlehem-view.jpg');
  background-size:cover;
  background-position: center;
	width: 100vw;
	height: calc(100vh - 3rem);
	align-content: center;
}

.environment-shout {
	max-width: fit-content;
  margin-inline: auto;
  color: var(--light-grey-color);
  text-align: center;
  font-weight: 500;
}

.environment-shout h2 {
	font-size: 10em;
	line-height: .85em;
	margin-bottom: .15em;
	font-weight: 500;
}

.environment-shout p {
	font-size: 1.5em;
}


.tile svg {
	max-width: fit-content;
  margin-inline: auto;
}

@media (min-width: 48rem) {
	.two-column-text {
		column-count: 2;
		column-gap: 4vw;
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
}

</style>