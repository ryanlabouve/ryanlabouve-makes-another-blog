<script lang="ts">
  import {twitterIcon, githubIcon, linkedinIcon} from '../services/icons';
  interface SocialLinkInterface {
    title: String,
    icon: String,
    link: String
  }

  const SOCIAL_LINKS : SocialLinkInterface[] = [
    {
      title: 'Twitter',
      icon: twitterIcon,
      link: 'https://twitter.com/ryanlabouve',
    },
    {
      title: 'Github',
      icon: githubIcon,
      link: 'https://github.com/ryanlabouve',
    },
    {
      title: 'LinkedIn',
      icon: linkedinIcon,
      link: 'https://www.linkedin.com/in/ryanlabouve',
    },
  ];
</script>
<div class="p-16">
  <h1 class="text-3xl pb-6">
    RyanLaBouve.com
  </h1>
  {#each SOCIAL_LINKS as {title, icon, link}}
    <div>
      <a class="flex my-2 -ml-7" href={link}>
        <div class="text-gray-800 dark:text-gray-200 fill-current opacity-80 mr-1">
          {@html icon}
        </div>
        {title}
      </a>
    </div>
  {/each}

  <div class="border border-t-1 border-white bg-opacity-50 my-12"></div>
  <p>
    I killed my old site on accident. Please hold while I— and I did try not to this time—re-write my blog.
  </p>
</div>