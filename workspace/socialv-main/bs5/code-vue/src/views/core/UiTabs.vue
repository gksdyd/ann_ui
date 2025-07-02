<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <b-card
            class="position-relative inner-page-bg bg-primary"
            style="height: 150px"
          >
            <div class="inner-page-title">
              <h3 class="text-white">Tabs Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </b-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Basic Tabs</h4>
            </template>

            <template v-slot:body>
              <p>
                The base <code>.nav</code> component does not include any
                <code>.active</code> state. The following examples include the
                class, mainly to demonstrate that this particular class does not
                trigger any special styling.
              </p>

              <tab-nav :tabs="true" id="myTab">
                <tab-nav-items
                  :active="true"
                  id="home-tab-one"
                  ariaControls="home"
                  href="#home-one"
                  role="tab"
                  :ariaSelected="true"
                  title="Home"
                />
                <tab-nav-items
                  :active="false"
                  id="profile-tab-one"
                  ariaControls="profile"
                  href="#profile-one"
                  role="tab"
                  :ariaSelected="false"
                  title="Profile"
                />
                <tab-nav-items
                  :active="false"
                  id="contact-tab-one"
                  ariaControls="contact"
                  href="#contact-one"
                  role="tab"
                  :ariaSelected="false"
                  title="Contact"
                />
              </tab-nav>
              <tab-content id="myTabContent-4">
                <tab-content-item
                  :active="true"
                  id="home-one"
                  aria-labelled-by="home-tab-one"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="profile-one"
                  aria-labelled-by="profile-tab-one"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="contact-one"
                  aria-labelled-by="contact-tab-one"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
              </tab-content>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Basic Tabs Style 3</h4>
            </template>

            <template v-slot:body>
              <p>
                Takes the basic nav from above and adds the
                <code>.nav-tabs</code> class to generate a tabbed interface.
              </p>

              <tab-nav :tabs="true" id="myTab-two">
                <tab-nav-items
                  :active="true"
                  id="home-tab-two"
                  ariaControls="home"
                  href="#home-two"
                  role="tab"
                  :ariaSelected="true"
                  title="Home"
                />
                <tab-nav-items
                  :active="false"
                  id="profile-tab-two"
                  ariaControls="profile"
                  href="#profile-two"
                  role="tab"
                  :ariaSelected="false"
                  title="Profile"
                />
                <tab-nav-items
                  :active="false"
                  id="contact-tab-two"
                  ariaControls="contact"
                  href="#contact-two"
                  role="tab"
                  :ariaSelected="false"
                  title="Contact"
                />
              </tab-nav>
              <tab-content id="myTabContent-1">
                <tab-content-item
                  :active="true"
                  id="home-two"
                  aria-labelled-by="home-tab-two"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="profile-two"
                  aria-labelled-by="profile-tab-two"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="contact-two"
                  aria-labelled-by="contact-tab-two"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
              </tab-content>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Tabs Vertical Pills</h4>
            </template>

            <template v-slot:body>
              <p>
                Stack your navigation by changing the flex item direction with
                the <code>.flex-column</code> utility.
              </p>

              <b-row>
                <b-col sm="3">
                  <tab-nav
                    :pills="true"
                    :vertical="true"
                    class="text-center"
                    id="v-pills-tab"
                  >
                    <tab-nav-items
                      :active="true"
                      id="v-pills-home-tab"
                      href="#v-pills-home"
                      ariaControls="v-pills-home"
                      role="tab"
                      :ariaSelected="true"
                      title="Home"
                    />
                    <tab-nav-items
                      :active="false"
                      id="v-pills-profile-tab"
                      href="#v-pills-profile"
                      ariaControls="v-pills-profile"
                      role="tab"
                      :ariaSelected="false"
                      title="Profile"
                    />
                    <tab-nav-items
                      :active="false"
                      id="v-pills-messages-tab"
                      href="#v-pills-messages"
                      ariaControls="v-pills-messages"
                      role="tab"
                      :ariaSelected="false"
                      title="Messages"
                    />
                    <tab-nav-items
                      :active="false"
                      id="v-pills-settings-tab"
                      href="#v-pills-settings"
                      ariaControls="v-pills-settings"
                      role="tab"
                      :ariaSelected="false"
                      title="Settings"
                    />
                  </tab-nav>
                </b-col>
                <b-col sm="9">
                  <tab-content id="v-pills-tabContent" class="mt-0">
                    <tab-content-item
                      :active="true"
                      id="v-pills-home"
                      aria-labelled-by="v-pills-home-tab"
                    >
                      <p>
                        Lorem Ipsum is simply dummy text of the printing and
                        typesetting industry. Lorem Ipsum has been the
                        industry's standard dummy text ever since the 1500s,
                        when an unknown printer took a galley of type and
                        scrambled it to make a type specimen book. It has
                        survived not only five centuries, but also the leap into
                        electronic typesetting, remaining essentially unchanged.
                      </p>
                    </tab-content-item>
                    <tab-content-item
                      :active="false"
                      id="v-pills-profile"
                      aria-labelled-by="v-pills-profile-tab"
                    >
                      <p>
                        Lorem Ipsum is simply dummy text of the printing and
                        typesetting industry. Lorem Ipsum has been the
                        industry's standard dummy text ever since the 1500s,
                        when an unknown printer took a galley of type and
                        scrambled it to make a type specimen book. It has
                        survived not only five centuries, but also the leap into
                        electronic typesetting, remaining essentially unchanged.
                      </p>
                    </tab-content-item>
                    <tab-content-item
                      :active="false"
                      id="v-pills-messages"
                      aria-labelled-by="v-pills-messages-tab"
                    >
                      <p>
                        Lorem Ipsum is simply dummy text of the printing and
                        typesetting industry. Lorem Ipsum has been the
                        industry's standard dummy text ever since the 1500s,
                        when an unknown printer took a galley of type and
                        scrambled it to make a type specimen book. It has
                        survived not only five centuries, but also the leap into
                        electronic typesetting, remaining essentially unchanged.
                      </p>
                    </tab-content-item>
                    <tab-content-item
                      :active="false"
                      id="v-pills-settings"
                      aria-labelled-by="v-pills-settings-tab"
                    >
                      <p>
                        Lorem Ipsum is simply dummy text of the printing and
                        typesetting industry. Lorem Ipsum has been the
                        industry's standard dummy text ever since the 1500s,
                        when an unknown printer took a galley of type and
                        scrambled it to make a type specimen book. It has
                        survived not only five centuries, but also the leap into
                        electronic typesetting, remaining essentially unchanged.
                      </p>
                    </tab-content-item>
                  </tab-content>
                </b-col>
              </b-row>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Tabs Justify Center</h4>
            </template>

            <template v-slot:body>
              <p>Centered with <code>.justify-content-center</code></p>

              <tab-nav :tabs="true" id="myTab-2" align="center">
                <tab-nav-items
                  :active="true"
                  id="home-tab-justify"
                  href="#home-justify"
                  ariaControls="home"
                  role="tab"
                  :ariaSelected="true"
                  title="Home"
                />
                <tab-nav-items
                  :active="false"
                  id="profile-tab-justify"
                  href="#profile-justify"
                  ariaControls="profile"
                  role="tab"
                  :ariaSelected="false"
                  title="Profile"
                />
                <tab-nav-items
                  :active="false"
                  id="contact-tab-justify"
                  href="#contact-justify"
                  ariaControls="contact"
                  role="tab"
                  :ariaSelected="false"
                  title="Contact"
                />
              </tab-nav>
              <tab-content id="myTabContent-3">
                <tab-content-item
                  :active="true"
                  id="home-justify"
                  aria-labelled-by="home-tab-justify"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="profile-justify"
                  aria-labelled-by="profile-tab-justify"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="contact-justify"
                  aria-labelled-by="contact-tab-justify"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
              </tab-content>
            </template>
          </iq-card>
        </b-col>
        <b-col lg="6" sm="12">
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Basic Tabs Style 2</h4>
            </template>

            <template v-slot:body>
              <p>
                Take that same HTML, but use <code>.nav-pills</code> instead:
              </p>

              <tab-nav :pills="true" id="pills-tab" class="mb-3">
                <tab-nav-items
                  :active="true"
                  id="pills-home-tab"
                  href="#pills-home"
                  ariaControls="pills-home"
                  role="tab"
                  :ariaSelected="true"
                  title="Home"
                />
                <tab-nav-items
                  :active="false"
                  id="pills-profile-tab"
                  href="#pills-profile"
                  ariaControls="pills-profile"
                  role="tab"
                  :ariaSelected="false"
                  title="Profile"
                />
                <tab-nav-items
                  :active="false"
                  id="pills-contact-tab"
                  href="#pills-contact"
                  ariaControls="pills-contact"
                  role="tab"
                  :ariaSelected="false"
                  title="Contact"
                />
              </tab-nav>
              <tab-content id="pills-tabContent-2">
                <tab-content-item
                  :active="true"
                  id="pills-home"
                  aria-labelled-by="pills-home-tab"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="pills-profile"
                  aria-labelled-by="pills-profile-tab"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="pills-contact"
                  aria-labelled-by="pills-contact-tab"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
              </tab-content>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Basic Tabs Style 4</h4>
            </template>

            <template v-slot:body>
              <p>
                Takes the basic nav from above and adds the
                <code>.nav-tabs</code> class to generate a tabbed interface.
              </p>

              <tab-nav :tabs="true" id="myTab-three">
                <tab-nav-items
                  :active="true"
                  id="home-tab-three"
                  ariaControls="home"
                  href="#home-three"
                  role="tab"
                  :ariaSelected="true"
                  title="Home"
                />
                <tab-nav-items
                  :active="false"
                  id="profile-tab-three"
                  ariaControls="profile"
                  href="#profile-three"
                  role="tab"
                  :ariaSelected="false"
                  title="Profile"
                />
                <tab-nav-items
                  :active="false"
                  id="contact-tab-three"
                  ariaControls="contact"
                  href="#contact-three"
                  role="tab"
                  :ariaSelected="false"
                  title="Contact"
                />
              </tab-nav>
              <tab-content id="myTabContent-4">
                <tab-content-item
                  :active="true"
                  id="home-three"
                  aria-labelled-by="home-tab-three"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="profile-three"
                  aria-labelled-by="profile-tab-three"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="contact-three"
                  aria-labelled-by="contact-tab-three"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
              </tab-content>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Tabs Fill And Justify</h4>
            </template>

            <template v-slot:body>
              <p>
                Force your <code>.nav</code>’s contents to extend the full
                available width one of two modifier classes. To proportionately
                fill all available space with your <code>.nav-item</code>s, use
                <code>.nav-fill</code>. Notice that all horizontal space is
                occupied, but not every nav item has the same width.
              </p>

              <tab-nav :pills="true" class="nav-fill mb-3" id="pills-tab-1">
                <tab-nav-items
                  :active="true"
                  id="pills-home-tab-fill"
                  href="#pills-home-fill"
                  ariaControls="pills-home-fill"
                  role="tab"
                  :ariaSelected="true"
                  title="Home"
                />
                <tab-nav-items
                  :active="false"
                  id="pills-profile-tab-fill"
                  href="#pills-profile-fill"
                  ariaControls="pills-profile-fill"
                  role="tab"
                  :ariaSelected="false"
                  title="Profile"
                />
                <tab-nav-items
                  :active="false"
                  id="pills-contact-tab-fill"
                  href="#pills-contact-fill"
                  ariaControls="pills-contact-fill"
                  role="tab"
                  :ariaSelected="false"
                  title="Contact"
                />
              </tab-nav>
              <tab-content id="pills-tabContent-1" class="mt-0">
                <tab-content-item
                  :active="true"
                  id="pills-home-fill"
                  aria-labelled-by="pills-home-tab-fill"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="pills-profile-fill"
                  aria-labelled-by="pills-profile-tab-fill"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="pills-contact-fill"
                  aria-labelled-by="pills-contact-tab-fill"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
              </tab-content>
            </template>
          </iq-card>
          <iq-card body-class="pt-0">
            <template v-slot:headerTitle>
              <h4 class="card-title">Tabs Justify Right</h4>
            </template>

            <template v-slot:body>
              <p>Right-aligned with <code>.justify-content-end</code>.</p>

              <tab-nav :tabs="true" id="myTab-4" align="end">
                <tab-nav-items
                  :active="true"
                  id="home-tab-end"
                  href="#home-end"
                  ariaControls="home"
                  role="tab"
                  :ariaSelected="true"
                  title="Home"
                />
                <tab-nav-items
                  :active="false"
                  id="profile-tab-end"
                  href="#profile-end"
                  ariaControls="profile"
                  role="tab"
                  :ariaSelected="false"
                  title="Profile"
                />
                <tab-nav-items
                  :active="false"
                  id="contact-tab-end"
                  href="#contact-end"
                  ariaControls="contact"
                  role="tab"
                  :ariaSelected="false"
                  title="Contact"
                />
              </tab-nav>
              <tab-content id="myTabContent-5">
                <tab-content-item
                  :active="true"
                  id="home-end"
                  aria-labelled-by="home-tab-end"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="profile-end"
                  aria-labelled-by="profile-tab-end"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
                <tab-content-item
                  :active="false"
                  id="contact-end"
                  aria-labelled-by="contact-tab-end"
                >
                  <p>
                    Lorem Ipsum is simply dummy text of the printing and
                    typesetting industry. Lorem Ipsum has been the industry's
                    standard dummy text ever since the 1500s, when an unknown
                    printer took a galley of type and scrambled it to make a
                    type specimen book.
                  </p>
                </tab-content-item>
              </tab-content>
            </template>
          </iq-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
// import { socialvue } from '../../config/pluginInit'
export default {
  name: "UiTabs",
  mounted() {
    // socialvue.index()
  },
};
</script>
