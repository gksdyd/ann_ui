<template>
  <div class="content-inner">
    <div class="container">
      <div class="row">
        <div class="mb-2">
          <h4>Popular apps</h4>
          <p>Explore the most installed apps in the HubSpot Marketplace</p>
        </div>
        <div
          v-for="(app, index) in apps"
          :key="index"
          class="col-sm-6 col-md-4"
        >
          <div class="card cardhover">
            <div class="card-body">
              <div>
                <img
                  :src="app.image"
                  class="avatar avatar-50 job-icon mb-3 d-inline-block"
                  loading="lazy"
                  alt="img"
                />
              </div>
              <h5>{{ app.name }}</h5>
              <small>Built by HubSpot</small>
              <div class="mt-2">
                <p class="mb-0">{{ app.description }}</p>
              </div>
              <span class="text-warning d-block line-height mt-0">
                <span class="text-warning d-flex align-items-center mt-2">
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 text-gray me-1"
                    >star</i
                  >
                  <small class="text-dark me-1">{{ app.rating }}</small>
                </span>
                <small class="mt-2">
                  <span
                    ><span>{{ app.installs }}</span
                    >+ installs</span
                  >
                </small>
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="my-2">
          <h4>New apps</h4>
          <p>Recent additions worth checking out</p>
        </div>
        <div v-for="app in newApps" :key="app.id" class="col-sm-6 col-md-4">
          <div class="card cardhover">
            <div class="card-body">
              <div>
                <img
                  :src="app.image"
                  class="avatar avatar-50 job-icon mb-3 d-inline-block"
                  loading="lazy"
                  alt="App Image"
                />
              </div>
              <h5>{{ app.name }}</h5>
              <small>Built by {{ app.developer }}</small>
              <div class="mt-2">
                <p class="mb-0">{{ app.description }}</p>
              </div>
              <div class="mt-4">
                <small>{{ app.status }}</small>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="my-2">
          <h4>Free apps</h4>
          <p>Explore free apps in the HubSpot Marketplace</p>
        </div>
        <div v-for="app in freeApps" :key="app.id" class="col-sm-6 col-md-4">
          <div class="card" :class="app.cardHover === true ? 'cardhover' : ''">
            <div class="card-body">
              <div>
                <img
                  :src="app.image"
                  class="avatar avatar-50 job-icon mb-3 d-inline-block"
                  loading="lazy"
                  alt="App Image"
                />
              </div>
              <h5>{{ app.name }}</h5>
              <small>Built by {{ app.developer }}</small>
              <div class="mt-1">
                <p class="mb-0">{{ app.description }}</p>
              </div>
              <div :class="app.mtclass === true ? 'mt-4' : 'mt-1'">
                <small
                  ><span>{{ app.installs }}</span
                  >+ installs</small
                >
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="my-2">
          <h4>Built By HubSpot</h4>
          <p>Explore apps built and supported by HubSpot</p>
        </div>
        <div
          v-for="(app, index) in builtapps"
          :key="index"
          class="col-sm-6 col-md-4"
        >
          <div class="card cardhover">
            <div class="card-body">
              <div>
                <img
                  :src="app.image"
                  class="avatar avatar-50 job-icon mb-3 d-inline-block"
                  loading="lazy"
                  alt="img"
                />
              </div>
              <h5>{{ app.name }}</h5>
              <small>Built by HubSpot</small>
              <div class="mt-2">
                <p class="mb-0">{{ app.description }}</p>
              </div>
              <span class="d-block line-height mt-0">
                <span class="text-warning d-flex align-items-center mt-2">
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 text-gray me-1"
                    >star</i
                  >
                  <small class="text-dark me-1">{{ app.rating }}</small>
                </span>
                <small class="mt-2">
                  <span
                    ><span>{{ app.installs }}</span
                    >+ installs</span
                  >
                </small>
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="my-2">
          <h4>Workflow Integrations</h4>
          <p>Explore apps you can leverage within HubSpot workflows.</p>
        </div>
        <div
          v-for="(app, index) in workflow"
          :key="index"
          class="col-sm-6 col-md-4"
        >
          <div class="card cardhover">
            <div class="card-body">
              <div>
                <img
                  :src="app.image"
                  class="avatar avatar-50 job-icon mb-3 d-inline-block"
                  loading="lazy"
                  alt="img"
                />
              </div>
              <h5>{{ app.name }}</h5>
              <small>{{ app.builtby }}</small>
              <div class="mt-2">
                <p class="mb-0">{{ app.description }}</p>
              </div>
              <span :class="[app.classTextwarning, 'd-block line-height mt-0']">
                <span class="text-warning d-flex align-items-center mt-2">
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 text-gray me-1"
                    >star</i
                  >
                  <small class="text-dark me-1">{{ app.rating }}</small>
                </span>
                <small class="mt-2">
                  <span
                    ><span>{{ app.installs }}</span
                    >+ installs</span
                  >
                </small>
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="my-2">
          <h4>Data Sync Built By HubSpot</h4>
          <p>
            Explore powerful and easy-to-use two-way data sync for 25+ apps,
            built by HubSpot
          </p>
        </div>
        <div
          v-for="(app, index) in datasync"
          :key="index"
          class="col-sm-6 col-md-4"
        >
          <div class="card cardhover">
            <div class="card-body">
              <div>
                <img
                  :src="app.image"
                  class="avatar avatar-50 job-icon mb-3 d-inline-block"
                  loading="lazy"
                  alt="img"
                />
              </div>
              <h5>{{ app.name }}</h5>
              <small>Built by HubSpot</small>
              <div class="mt-2">
                <p class="mb-0">{{ app.description }}</p>
              </div>
              <span :class="[app.classTextwarning, 'd-block line-height mt-0']">
                <span class="text-warning d-flex align-items-center mt-2">
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 me-1">star</i>
                  <i class="material-symbols-outlined md-18 text-gray me-1"
                    >star</i
                  >
                  <small class="text-dark me-1">{{ app.rating }}</small>
                </span>
                <small class="mt-2">
                  <span
                    ><span>{{ app.installs }}</span
                    >+ installs</span
                  >
                </small>
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="my-2">
          <h4>Marketing Campaign Apps</h4>
          <p>
            Explore apps that can help optimize your marketing campaign efforts
            in HubSpot.
          </p>
        </div>
        <div
          v-for="(app, index) in marketapps"
          :key="index"
          class="col-sm-6 col-md-4"
        >
          <div class="card cardhover">
            <div class="card-body">
              <div>
                <img
                  :src="app.image"
                  class="avatar avatar-50 job-icon mb-3 d-inline-block"
                  loading="lazy"
                  alt="img"
                />
              </div>
              <h5>{{ app.name }}</h5>
              <small>{{ app.builtby }}</small>
              <div class="mt-2">
                <p :class="app.mbclass === true ? 'mb-0' : 'mt-2'">
                  {{ app.description }}
                </p>
              </div>
              <span class="text-warning d-flex align-items-center mt-2">
                <i class="material-symbols-outlined md-18 me-1">star</i>
                <i class="material-symbols-outlined md-18 me-1">star</i>
                <i class="material-symbols-outlined md-18 me-1">star</i>
                <i class="material-symbols-outlined md-18 me-1">star</i>
                <i class="material-symbols-outlined md-18 text-gray me-1"
                  >star</i
                >
                <small class="text-dark me-1">{{ app.rating }}</small>
              </span>
              <small class="mt-2">
                <span
                  ><span>{{ app.installs }}</span
                  >+ installs</span
                >
              </small>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="my-2">
          <h4>Media Bridge Apps</h4>
          <p>
            Combine the power of HubSpot’s CRM platform with your favorite media
            apps
          </p>
        </div>
        <div
          v-for="(app, index) in bridgeapps"
          :key="index"
          class="col-sm-6 col-md-4"
        >
          <div class="card cardhover">
            <div class="card-body">
              <div>
                <img
                  :src="app.image"
                  class="avatar avatar-50 job-icon mb-3 d-inline-block"
                  loading="lazy"
                  alt="img"
                />
              </div>
              <h5>{{ app.name }}</h5>
              <small>Built by HubSpot</small>
              <div class="mt-2">
                <p class="mb-0">{{ app.description }}</p>
              </div>
              <!-- <span class="text-warning d-block line-height mt-0"> -->
              <span class="text-warning d-flex align-items-center mt-2">
                <i class="material-symbols-outlined md-18 me-1">star</i>
                <i class="material-symbols-outlined md-18 me-1">star</i>
                <i class="material-symbols-outlined md-18 me-1">star</i>
                <i class="material-symbols-outlined md-18 me-1">star</i>
                <i class="material-symbols-outlined md-18 text-gray me-1"
                  >star</i
                >
                <small class="text-dark me-1">{{ app.rating }}</small>
              </span>
              <div class="">
                <small>
                  <span
                    ><span>{{ app.installs }}</span
                    >+ installs</span
                  >
                </small>
              </div>
              <!-- </span> -->
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "market1",
      apps: [
        {
          id: 1,
          name: "Gmail",
          image: require("@/assets/images/market/1.png"),
          description:
            "Bring HubSpot to your inbox with the HubSpot integration for Gmail.",
          rating: 400,
          installs: "10,000",
        },
        {
          id: 2,
          name: "Google Calendar",
          image: require("@/assets/images/market/2.png"),
          description:
            "Bring HubSpot to your inbox with the HubSpot integration for Gmail.",
          rating: 189,
          installs: "10,000",
        },
        {
          id: 3,
          name: "HubSpot for WordPress",
          image: require("@/assets/images/market/8.png"),
          description:
            "Integrate HubSpot's lead capture and contact management with WordPress",
          rating: 61,
          installs: "10,000",
        },
      ],
      newApps: [
        {
          id: 1,
          name: "Channelyze",
          image: require("@/assets/images/market/3.png"),
          developer: "Channelyze Ltd",
          description:
            "Manage channel sales and partner renewals through HubSpot.",
          status: "New",
        },
        {
          id: 2,
          name: "Showpad by Elixir Solutions",
          image: require("@/assets/images/market/3.png"),
          developer: "Elixir Solutions",
          description: "Add Showpad email activity in HubSpot",
          status: "New",
        },
        {
          id: 3,
          name: "Ion by Rock Content",
          image: require("@/assets/images/market/3.png"),
          developer: "Rock Content",
          description: "Content experiences your audience will love",
          status: "New",
        },
      ],
      freeApps: [
        {
          id: 1,
          name: "Alexa Helper",
          image: require("@/assets/images/market/3.png"),
          developer: "Voicify",
          description:
            "Access your HubSpot data in real time through Amazon's Alexa",
          installs: 50,
          mtclass: true,
          cardHover: false,
        },
        {
          id: 2,
          name: "Magento 2 Sync by Unific",
          image: require("@/assets/images/market/3.png"),
          developer: "Unific | HubSpot Ecommerce Integrations",
          description: "Take Data Driven Actions With Enriched Ecommerce Data",
          installs: 40,
          mtclass: false,
          cardHover: true,
        },
        {
          id: 3,
          name: "Pendo for HubSpot",
          image: require("@/assets/images/market/3.png"),
          developer: "Pendo",
          description: "Create product experiences people love",
          installs: 50,
          mtclass: true,
          cardHover: true,
        },
      ],
      builtapps: [
        {
          id: 1,
          name: "Facebook Messenger",
          image: require("@/assets/images/market/5.png"),
          description: "Manage all Messenger conversations and bots in HubSpot",
          rating: 21,
          installs: "10,000",
        },
        {
          id: 2,
          name: "Airtable",
          image: require("@/assets/images/market/3.png"),
          description:
            "Data Sync - Sync Airtable rows (with emails) with HubSpot",
          rating: 3,
          installs: "500",
        },
        {
          id: 3,
          name: "Mailchimp",
          image: require("@/assets/images/market/9.png"),
          description:
            "Data Sync - Sync contacts two-way with a Mailchimp Audience",
          rating: 22,
          installs: "3,500",
        },
      ],
      workflow: [
        {
          id: 1,
          name: "360NRS",
          image: require("@/assets/images/market/3.png"),
          builtby: "Built by Net Real Solutions",
          description:
            "Send individual SMS to your contacts or use workflows to send bulk SMS",
          rating: 3,
          classTextwarning: "text-warning",
          installs: "50",
        },
        {
          id: 2,
          name: "Aloware",
          image: require("@/assets/images/market/3.png"),
          builtby: "Built by Aloware",
          description:
            "Dialer, calling & texting automations with real-time logging & syncing",
          rating: 4,
          classTextwarning: "text-warning",
          installs: "100",
        },
        {
          id: 3,
          name: "SMS For HubSpot",
          image: require("@/assets/images/market/3.png"),
          builtby: "Built by MessageMedia",
          description:
            "Send and receive SMS without leaving HubSpot. Get started in minutes.",
          rating: 13,
          installs: "300",
        },
      ],
      datasync: [
        {
          id: 1,
          name: "Google Contacts",
          image: require("@/assets/images/market/7.png"),
          description: "Sync Google Contacts with HubSpot contacts",
          rating: 50,
          classTextwarning: "text-warning",
          installs: "9000",
        },
        {
          id: 2,
          name: "Mailchimp",
          image: require("@/assets/images/market/9.png"),
          description:
            "Data Sync - Sync contacts two-way with a Mailchimp Audience",
          rating: 22,
          classTextwarning: "text-warning",
          installs: "3,500",
        },
        {
          id: 3,
          name: "Stripe",
          image: require("@/assets/images/market/3.png"),
          description: "Data Sync - Sync Stripe and HubSpot customers",
          rating: 10,
          installs: "1,000",
        },
      ],
      marketapps: [
        {
          id: 1,
          name: "Databox",
          image: require("@/assets/images/market/3.png"),
          builtby: "Built by Databox, Inc",
          description:
            "Popular KPI/Analytics Dashboards Amongst HubSpot Customers",
          rating: 35,
          installs: "10,000",
          mbclass: true,
        },
        {
          id: 2,
          name: "Forminator",
          image: require("@/assets/images/market/3.png"),
          builtby: "Built by WPMU DEV",
          description:
            "Easy-to-create forms, polls, and quizzes for WordPress.",
          rating: 3,
          installs: "1,000",
          mbclass: true,
        },
        {
          id: 3,
          name: "Lucky Orange",
          image: require("@/assets/images/market/3.png"),
          builtby: "Built by HubSpot",
          description: "Improve customer experience with recordings",
          rating: 16,
          installs: "1,500",
          mbclass: false,
        },
      ],
      bridgeapps: [
        {
          id: 1,
          name: "Wistia",
          image: require("@/assets/images/market/3.png"),
          description: "Sync Google Contacts with HubSpot contacts",
          rating: 50,
          installs: "9000",
        },
        {
          id: 2,
          name: "Mailchimp",
          image: require("@/assets/images/market/9.png"),
          description:
            "Data Sync - Sync contacts two-way with a Mailchimp Audience",
          rating: 22,
          installs: "3,500",
        },
        {
          id: 3,
          name: "Stripe",
          image: require("@/assets/images/market/3.png"),
          description: "Data Sync - Sync Stripe and HubSpot customers",
          rating: 10,
          installs: "1,000",
        },
      ],
    };
  },
};
</script>
