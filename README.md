# html-progress-steps

<div style="display: flex; flex-direction: row">
  <div class="step completed">
    <div class="step-content">
      <span class="step-title">Olha o passo</span>
    </div>
  </div>
  <div class="step completed">
    <div class="arrow-right"></div>
    <div class="step-content">
      <span class="step-title">Olha o passo</span>
    </div>
  </div>
  <div class="step completed">
    <div class="arrow-right"></div>
    <div class="step-content">
      <span class="step-title">Passo</span>
    </div>
  </div>
  <div class="step active">
    <div class="arrow-right"></div>
    <div class="step-content">
      <span class="step-title">Olha o passo</span>
    </div>
  </div>
  <div class="step inactive">
    <div class="arrow-right"></div>
    <div class="step-content">
      <span class="step-title">Olha o passo</span>
    </div>
  </div>
</div>


.step {
  display: flex;
  flex-direction: row;
  background-color: lightgray
}

.step-content {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 200px;
}

.step-title {
  font-family: sans-serif;
  font-size: 19px
}

.step.active {
  background-color: green
}
.step.active .arrow-right {
  border-left: 25px solid green;
}
.step.completed + .step.active .arrow-right {
  border-left: 25px solid lightgreen;
  border-top: 22px solid green;
  border-bottom: 22px solid green;
}


.step.completed {
  background-color: lightgreen
}
.step.completed .arrow-right {
  border-left: 25px solid transparent;
  border-top: 22px solid transparent;
  border-bottom: 22px solid transparent;
}
.step.active + .step.completed .arrow-right {
  border-left: 25px solid green;
  border-top: 22px solid transparent;
  border-bottom: 22px solid transparent;
}


.step.inactive .arrow-right {
  border-top: 22px solid lightgray;
  border-bottom: 22px solid lightgray;
  border-left: 25px solid lightgray;
}
.step.active + .step.inactive .arrow-right {
  border-top: 22px solid lightgray;
  border-bottom: 22px solid lightgray;
  border-left: 25px solid green;
}
.step.completed + .step.inactive .arrow-right {
  border-top: 22px solid lightgray;
  border-bottom: 22px solid lightgray;
  border-left: 25px solid lightgreen;
}
