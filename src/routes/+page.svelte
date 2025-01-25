<script lang="ts">
	import { onMount } from 'svelte';
  import Logo from '$components/Logo.svelte';
  import Lung from '$components/Lung.svelte';
  import Plurality from '$components/Plurality.svelte';
  import Specialists from '$components/Specialists.svelte';
  import { inview } from 'svelte-inview';
  let showheader: boolean;
  let headertext = '';
  const options = {threshold: '.1'};
  const sectionoptions = {threshold: '.4'};  
</script>

<header class="showheader" class:showheader>
  <a
  class="logo"
  aria-label="Menu"
  href=''
  rel="noopener noreferrer"
  > <Logo /></a>
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
			<h1>Breathe,<br /> Allentown.</h1>
	</div>
	<div class="down">
		<a href=""></a>
	</div>
</section>

<section
class="introduction"
use:inview={sectionoptions}
on:inview_enter={(event) => {
      headertext = 'Introduction';
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
	<h3>Smoking and Asthma</h3>
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
		In the Allentown Bethlehem Easton metro area, there is only one specialist for every 100,000 patients. 
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
    }}
>

<div class="environment">
	<div class="environment-shout standard-padding">
		<h2>43%</h2>
		<p>of housing stock has issues that contribute to poor health.
	</div>
</div>

<div class="grid standard-padding no-gutter">
	<div class="width-12-12-m width-12-12-i width-12-12">
	<h3>Risk Factor: Housing Concerns</h3>
			<div class="two-column-text">
			<p class="lede">Much of the housing stock in the Allentown, Bethlehem and Easton metro area was developed for factory worker families of the early to mid 20th century. While it can be said that many of these houses were constructed with a pride of craft and longevity in mind, there are concerns related to old infrastructure. Leaks, poor or dirty ventilation, peeling paint, clunky old furnaces and oil burners all contribute to poor living conditions.</p>

			<p>As houses age, insulation settles, and leaks develop, hidden spaces become susceptible to mold. For people with chronic conditions, triggers and allergens in the home (such as dust, pests, and mold) can cause asthma and allergy symptoms. Remediation and renovation is expensive work. For many, perhaps the best course of action is to address issues as they occur in rooms most used.</p>

			<p>
				What else can be done? Laws that encourage landlords to address housing issues that impact health is one way forward. Programs that aid and incentivize propoerty owners to make much needed repairs is another. Improving the living envirnonments of the places we inhabit is doable. It's worth looking to examples like DC Healthy Housing Collaborative (DCHHS), and California Asthma Financing Workgroup.
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
  overflow-y: scroll;
  background-image: url('/img/a-map.jpg');
  background-size:cover;
  background-position: center;
  padding: 3em;
  display: flex;
  align-items: center;
}

.head {
	padding-top: 7em;
	background-image: url('/img/puff.svg');
	background-repeat: no-repeat;
	background-size: 8em 8em;
	background-position: right .5em top .5em;
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