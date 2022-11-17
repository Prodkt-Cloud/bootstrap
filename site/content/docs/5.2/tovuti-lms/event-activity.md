---
layout: docs
title: Event Activity
description:
group: extend
toc: true
---
## In Review

- Designer: Bryan Funk
- Product Owner: John Meindersee
<!-- markdownlint-disable -->
{{< example >}}
<div class="tovAx__componentQuery__container d-flex flex-column h-100 w-100 gap-4">
<div class="w-100 p-0 rounded" style="background-image: url('/docs/5.2/assets/img/placeholder_component.svg');  width: 100%; height:96px;  background-position: 50% 44%; background-size: fill; background-attachment: fixed;"></div>
<div class="d-flex flex-row w-100 gap-4">
<div class="dragTovAxSideNavWrapper rounded mh-100" style="background-image: url('/docs/5.2/assets/img/placeholder_component.svg'); background-attachment: fixed; width: 220px;">
<div class="dragTovAxSideNav rounded h-100 mw-100" style=""></div>
</div>
<div class="d-flex flex-sm-row-reverse flex-lg-row flex-wrap align-items-top gap-4">
<div class="w-100 p-0 rounded" style="background-image: url('/docs/5.2/assets/img/placeholder_component.svg'); max-width: 240px; min-width: 100%; height:96px;  background-position: 50% 44%; background-size: fill; background-attachment: fixed;"></div>
  <div class="col-12 col-md-8 flex-fill position-relative">
    <div class="position-absolute top-0 translate-middle btn-group gap-2 w-auto" role="group"
      aria-label="Horizontal radio toggle button group justify-content-end"
      style="z-index:10; left: auto; right: -100px;">
      <input type="radio" class="btn-check" name="vbtn-radio1" id="vbtn-radio1" autocomplete="off" checked>
      <label class="btn d-inline-flex align-items-center bg-danger rounded-pill text-light border-0"
        for="vbtn-radio1"><i class="fa fa-circle-xmark me-2"></i>Required</label>
      <input type="radio" class="btn-check" name="vbtn-radio2" id="vbtn-radio2" autocomplete="off">
      <label class="btn d-inline-flex align-items-center bg-success rounded-pill text-light border-0"
        for="vbtn-radio2"><i class="fa fa-circle-check me-2"></i>Complete</label>
    </div>
    <div class="tov-lessonActivity-event border rounded shadow-sm overflow-hidden">
      <div class="card border-0">
        <div class="row g-0">
          <div class="tov-lessonActivity-event_coverImgage col-3 border border-0 position-relative">
            <img src="/docs/5.2/assets/img/placeholder.svg"
              class="border-0 object-fit-cover img-fluid border-0" style="background-position: center center;">
          </div>
          <div class=" col-12 col-lg-9 flex-fill p-0">
            <div class="card-body p-0">
              <div class="p-4 text-start">
                <h5 class="card-title" contenteditable="true">$eventTitle<div class="isEditable"></div>
                </h5>
                <p class="position-relative mb-0" contenteditable="true">$short-description<span
                    class="isEditable"></span></p>
              </div>
              <div class="hstack flex-wrap gap-1 p-3 w-100 border-top">
                <div class="d-flex flex-wrap" x-data="{ value: ['11/09/2022'],
                              init() {
                                  let picker = flatpickr(this.$refs.picker, {
                                      dateFormat: 'm/d/Y',
                                      defaultDate: this.value,
                                      onChange: (date, dateString) => {
                                          this.value = dateString.split(' to ')  } })
                                  this.$watch('value', () => picker.setDate(this.value)) }, }">
                  <p class="ps-2 py-2 my-0"><i class="fa fa-calendar me-2"></i><em
                      class="fw-bold fst-normal me-1">$date:</em></p>
                  <input class="border-0 ps-0 w-auto" x-ref="picker" type="text">
                </div>
                <div class="d-flex flex-wrap w-100 justify-content-start" x-data="{ value: ['11/09/2022', ' 11/27/2022'],
                              init() {
                                  let picker = flatpickr(this.$refs.picker, {
                                       mode: 'range',
                                      dateFormat: 'm/d/Y',
                                      defaultDate: this.value,
                                      onChange: (date, dateString) => {
                                          this.value = dateString.split(' to ')  } })
                                  this.$watch('value', () => picker.setDate(this.value)) }, }">
                  <p class="ps-2 py-2 my-0 text-start"><i class="fa fa-calendar me-2"></i><em
                      class="fw-bold fst-normal me-1">$dateRange:</em></p>
                  <input class="border-0 ps-0 w-auto align-item-start" x-ref="picker" type="text">
                </div>
                <p
                  class="d-flex flex-wrap w-100 justify-content-start align-items-center ps-2 py-2 my-0 gap-0 text-start">
                  <i class="fa fa-circle-dollar me-2"></i><em class="fw-bold fst-normal me-1">Price/per
                    registrant:</em>$price</p>
                <p class="ps-2 py-2 my-0 text-start w-100"><i class="fa fa-clock me-2"></i><em
                    class="fw-bold fst-normal me-1 w-100">Start time:</em>$time $anteMeridiem, $timeZone</p>
                <p class="ps-2 py-2 my-0 text-start w-100"><i class="fa fa-alarm-clock me-2"></i><em
                    class="fw-bold fst-normal me-1">End time:</em>$time $anteMeridiem, $timeZone</p>
                <p class="ps-2 py-2 my-0 text-start"><i class="fa fa-map me-2"></i><em
                    class="fw-bold fst-normal me-1">Where:</em><a href="">Get Directions to this Event</a></p>
                <button type="button"
                  class="d-flex flex-wrap justify-content-start align-items-center gap-2 btn btn-link ps-2 py-2 w-100 text-start fw-semibold"><img
                    src="/docs/5.2/assets/img/tovuti/logos/teams.svg"
                    class="object-fit-cover img-fluid text-decoration-none" style="height: 16px;">Join with Microsoft
                  Teams</button>
                <button type="button"
                  class="d-flex flex-wrap justify-content-start align-items-center gap-2 btn btn-link ps-2 py-2 w-100 text-start fw-semibold"><img
                    src="/docs/5.2/assets/img/tovuti/logos/g-meet.svg"
                    class="object-fit-cover img-fluid text-decoration-none" style="height: 16px;">Join with Google
                  Meet</button>
                <p
                  class="d-flex flex-wrap justify-content-start align-items-center gap-2 btn btn-link ps-2 py-2 w-100 text-start text-decoration-none fw-semibold">
                  <i class="fa fa-circle-video"></i><span class="text-decoration-underline">Join Virtual
                    Classroom</span></p>
              </div>
              <div
                class="vstack bg-light flex-wrap gap-2 p-3 w-100 border-top align-items-bottom justify-content-start h-100">
                <button type="button"
                  class="btn btn-primary text-decoration-none d-flex flex-fill gap-2 justify-content-center align-items-center"><i
                    class="fa fa-right-to-bracket"></i>Register for this Event</button>
                <button type="button"
                  class="btn btn-brand-white border text-black text-decoration-none d-flex gap-2 justify-content-center align-items-center ps-2"><i
                    class="fa fa-arrow-right"></i>More Details</button>
              </div>
              <div
                class="vstack bg-light flex-wrap gap-2 p-3 w-100 border-top align-items-bottom justify-content-between h-100">
                <span
                  class="bg-danger bg-opacity-10 p-2 rounded text-danger text-decoration-none d-flex flex-fill gap-2 justify-content-center align-items-center"><i
                    class="fa fa-circle-xmark"></i>Event is at max capacity</span>
                <span class="text-start py-2">Would you like to be added to the Waitlist? If a spot does become available you
                  will be added as a registered attendee to this event.</span>
                <button type="button"
                  class=" border text-decoration-none d-flex gap-2 justify-content-center align-items-center ps-2" x-data="{ status: false, status2: false }" x-on:click="status = !status" :class="status ? 'btn bg-success border-success bg-opacity-100 text-white' : 'btn bg-warning border-warning bg-opacity-10'"><i
                    class="fa fa-circle-check text-white" :class="status ? '' : 'd-none'"></i><span class="text-start fs-6" x-text="status ? 'You are on the waiting list!': 'Join the Waiting List'"></span></button>
                <button type="button"
                  class="btn btn-brand-white border text-black text-decoration-none d-flex gap-2 justify-content-center align-items-center ps-2"><i
                    class="fa fa-arrow-right"></i>More Details</button>
              </div>
              <div
                class="vstack bg-success flex-wrap gap-3 p-3 w-100 border-top align-items-bottom justify-content-between h-100">
                <span
                  class="text-decoration-none d-flex gap-2 text-light justify-content-center align-items-center "><i
                    class="fa-solid fa-check"></i>You're Registered for this Event!</span>
                <button type="button"
                  class="btn btn-light text-black text-decoration-none d-flex gap-2 justify-content-center align-items-center"><i
                    class="fa fa-arrow-right"></i>More Details</button>
              </div>
              <div class="calContainer hstack flex-wrap gap-1 px-2 py-3 w-100 border-top justify-content-evenly text-center"><span
                  class="w-100 mb-2">Add this to your calendar</span>
                <div class="hstack flex-wrap w-100 gap-0 gap-md-3 justify-content-center text-center"><a
                    href="#" data-type="google"><img src="/docs/5.2/assets/img/tovuti/calendar/calendar_google.svg"
                      class="w-auto" style="height:32px;" data-type="google"></a>
                  <div class="vr"></div><a href="#" data-type="ics"><img
                      src="/docs/5.2/assets/img/tovuti/calendar/calendar_iCloud.svg" class="w-auto"
                      style="height:32px;"></a>
                  <div class="vr"></div><a href="#" data-type="yahoo"><img
                      src="/docs/5.2/assets/img/tovuti/calendar/calendar_yahoo.svg" class="w-auto"
                      style="height:32px;"></a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="w-auto flex-grow-1">
    <div class="tovAx__lesson--nextLessonCard position-sticky d-flex flex-fill bg-light flex-column p-0 rounded shadow-sm">

    </div>
  </div>
</div>
<!-- END COMPONENT QUERY WRAPPER DIRECTLY AFTER THIS-->
</div>
<!-- END COMPONENT QUERY CONTAINER DIRECTLY AFTER THIS-->
</div>
{{< /example >}}

<!-- markdownlint-restore -->
