<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <div class="card position-relative inner-page-bg bg-primary" style="height: 150px">
            <div class="inner-page-title">
              <h3 class="text-white">Pricing 1</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </div>
        </b-col>
        <b-col sm="12">
          <iq-card>
            <template v-slot:body>
              <div class="table-responsive">
                <table class="table">
                  <thead>
                    <tr>
                      <th class="text-center" scope="col"></th>
                      <th class="text-center" scope="col">Starter</th>
                      <th class="text-center" scope="col">Business</th>
                      <th class="text-center" scope="col">Enterprise</th>
                      <th class="text-center" scope="col">Unlimited</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <th class="text-center" scope="row">Email support</th>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                    </tr>
                    <tr>
                      <th class="text-center" scope="row">UI Kit</th>
                      <td class="text-center"></td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                    </tr>
                    <tr>
                      <th class="text-center" scope="row">100% support</th>
                      <td class="text-center"></td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                    </tr>
                    <tr>
                      <th class="text-center" scope="row">Advance form</th>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                    </tr>
                    <tr>
                      <th class="text-center" scope="row">Custom shortcode</th>
                      <td class="text-center"></td>
                      <td class="text-center"></td>
                      <td class="text-center"></td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                    </tr>
                    <tr>
                      <th class="text-center" scope="row">
                        Thousand of Widgets
                      </th>
                      <td class="text-center"></td>
                      <td class="text-center"></td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                      <td class="text-center">
                        <i class="material-symbols-outlined text-success md-32">
                          check
                        </i>
                      </td>
                    </tr>
                    <tr>
                      <td class="text-center"></td>
                      <td class="text-center">
                        <h3 class="text-center">
                          $19<small class="font-size-12"> / Per month</small>
                        </h3>
                        <button type="button" class="btn btn-primary mt-3">
                          Purchase
                        </button>
                      </td>
                      <td class="text-center">
                        <h3 class="text-center">
                          $39<small class="font-size-12"> / Per month</small>
                        </h3>
                        <button type="button" class="btn btn-primary mt-3">
                          Purchase
                        </button>
                      </td>
                      <td class="text-center">
                        <h3 class="text-center">
                          $119<small class="font-size-12"> / Per month</small>
                        </h3>
                        <button type="button" class="btn btn-primary mt-3">
                          Purchase
                        </button>
                      </td>
                      <td class="text-center">
                        <h3 class="text-center">
                          $219<small class="font-size-12"> / Per month</small>
                        </h3>
                        <button type="button" class="btn btn-primary mt-3">
                          Purchase
                        </button>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </template>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>

export default {
  name: "Pricing",
  mounted() {
  },
  data() {
    return {
      headerColumn: [
        {
          key: "name",
          label: "",
        },
        {
          key: "starter",
          label: "Starter",
        },
        {
          key: "business",
          label: "Business",
        },
        {
          key: "enterprise",
          label: "Enterprise",
        },
        {
          key: "unlimited",
          label: "Unlimited",
        },
      ],
      rows: [
        {
          name: "Email support",
          starter: true,
          business: true,
          enterprise: true,
          unlimited: true,
        },
        {
          name: "UI Kit",
          starter: false,
          business: true,
          enterprise: true,
          unlimited: true,
        },
        {
          name: "100% support",
          starter: false,
          business: true,
          enterprise: true,
          unlimited: true,
        },
        {
          name: "Advance form",
          starter: true,
          business: true,
          enterprise: true,
          unlimited: true,
        },
        {
          name: "Custom shortcode",
          starter: false,
          business: false,
          enterprise: false,
          unlimited: true,
        },
        {
          name: "Thousand of Widgets",
          starter: false,
          business: false,
          enterprise: true,
          unlimited: true,
        },
        {
          name: "",
          button: true,
          starter: "$19/",
          starter_per: " Per month",
          business: "$39/",
          business_per: " Per month",
          enterprise: "$119/",
          enterprise_per: " Per month",
          unlimited: "$219/",
          unlimited_per: " Per month",
        },
      ],
    };
  },
};
</script>
