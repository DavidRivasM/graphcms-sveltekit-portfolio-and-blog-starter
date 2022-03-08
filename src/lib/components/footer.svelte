<script context="module">
  import {
    authorsStore,
    fetchAuthors,
    
  } from '$stores/site-metadata'
  import LinkedinIcon from './linkedin-icon.svelte'
  import GmailIcon from './gmail-icon.svelte'
  import WhatsappIcon from './whatsapp-icon.svelte'
  import GithubIcon from './github-icon.svelte'


  fetchAuthors()
</script>

<script>
  const { name: AuthorName } = $authorsStore
</script>

<footer
  class="p-10 footer bg-primary text-primary-content footer-center"
>
  <div class="grid grid-flow-col gap-4">
    <a class="link link-hover" href="/projects">Portfolio</a>
    <a class="link link-hover" href="/posts">Blog</a>
    <a class="link link-hover" href="/about">About</a>
  </div>
  <div>
    <div class="grid grid-flow-col gap-4">
      <a class="hover:scale-110 transition duration-300" href="mailto:alonsorivasmora@gmail.com" target="_blank" rel="noreferrer noopener">
        <GmailIcon />
      </a>
      <a class="hover:scale-110 transition duration-300" href="https://wa.me/50685255893?text=¡Hi%20David!%20I%20saw%20your%20online%20Portfolio.%20" target="_blank" rel="noreferrer noopener">
        <WhatsappIcon />
      </a>
      <a class="hover:scale-110 transition duration-300" href="https://www.linkedin.com/in/david-alonso-rivas-mora-24b606170/" target="_blank" rel="noreferrer noopener">
        <LinkedinIcon />
      </a>
      <a class="hover:scale-110 transition duration-300" href="https://github.com/DavidRivasM" target="_blank" rel="noreferrer noopener">
        <GithubIcon />
      </a>
    </div>
  </div>
  <div>
    <p>
      Copyright &copy; {`${new Date().getFullYear()}`} - All right reserved
      {AuthorName}
    </p>
  </div>
</footer>
