<template>
    <div>
        <slot/>
    </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
    body {
        font-family: Avenir, Roboto,"Helvetica Neue",Arial,sans-serif;
        margin:0;
        padding:0;
        line-height: 1.5;
    }

    #hb_embed_signup {
        margin: 0 auto;
        width: 100%;
        max-width: 500rem !important;
    }
</style>
