<template>
  <div class="haederSection">
    <div>
      <!-- As a heading -->

      <b-navbar variant="faded" type="light">
        <b-navbar-brand tag="h1" class="mb-0 ml-auto">
          <b-nav-form>
            <b-form-input placeholder="Search"></b-form-input>
            <b-button class="mx-2" type="submit">Search</b-button>

            <b-avatar variant="danger"></b-avatar>
          </b-nav-form>
        </b-navbar-brand>
      </b-navbar>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.haederSection {
  grid-area: haederSection;
  margin-top: 10px;
  margin-right: 10px;
  text-align: left;
}
</style>
