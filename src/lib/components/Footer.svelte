<script>
  import { Footer, FooterLinkGroup, FooterLink, FooterBrand, FooterIcon, FooterCopyright } from 'flowbite-svelte';
  import { FacebookSolid, GithubSolid, DiscordSolid, TwitterSolid } from 'flowbite-svelte-icons';
</script>

<Footer footerType="sitemap">
  <div class="grid grid-cols-2 gap-8 py-8 px-6 md:grid-cols-4">
    <div>
      <h2 class="mb-6 text-lg font-semibold text-gray-400 uppercase">CONNECT WITH US</h2>
      <FooterLinkGroup ulClass="text-gray-300">
        <FooterLink liClass="mb-1" href="/">Fr. Agnel Ashram, Bandstand Bandra(W). Mumbai400 050. MH. IN</FooterLink>
        <FooterLink liClass="mb-1" href="/">+91 22-6711 4000</FooterLink>
        <FooterLink liClass="mb-1" href="/">+91 22-6711 4100</FooterLink>
        <FooterLink liClass="mb-1 text-primary-400 " >crce@frcrce.ac.in</FooterLink>
      </FooterLinkGroup>
    </div>
    <div>
      <h2 class="mb-6 text-lg font-semibold uppercase text-gray-400">Staff Services</h2>
      <FooterLinkGroup ulClass="text-gray-300">
        <FooterLink liClass="mb-1" href="/">Agnel Mail Service</FooterLink>
        <FooterLink liClass="mb-1" href="/">Biometric Attendence Service</FooterLink>
        <FooterLink liClass="mb-1" href="/">Other Services</FooterLink>
        <FooterLink liClass="mb-1" href="/">Site Login</FooterLink>
        <FooterLink liClass="mb-1" href="/">Invigilation slot preference</FooterLink>
      </FooterLinkGroup>
    </div>
    <div>
      <h2 class="mb-6 text-lg font-semibold uppercase text-gray-400">Resources</h2>
      <FooterLinkGroup ulClass="text-gray-300">
        <FooterLink liClass="mb-1" href="/">TInkering Lab</FooterLink>
        <FooterLink liClass="mb-1" href="/">Moodle Access</FooterLink>
        <FooterLink liClass="mb-1" href="/">Student Portal</FooterLink>
        <FooterLink liClass="mb-1" href="/">Student Notices</FooterLink>
        <FooterLink liClass="mb-1" href="/">Student handbook- essential of ethics</FooterLink>
        <FooterLink liClass="mb-1" href="/">Downloads</FooterLink>
        <FooterLink liClass="mb-1" href="/">Audited Statements</FooterLink>
        <FooterLink liClass="mb-1" href="/">Institutions Innovation Cell</FooterLink>
        <FooterLink liClass="mb-1" href="/">Preincubation Details</FooterLink>
        <FooterLink liClass="mb-1" href="/">IPR cell</FooterLink>
        <FooterLink liClass="mb-1" href="/">Green Practices</FooterLink>
        <FooterLink liClass="mb-1" href="/">Facilites for Divangjan</FooterLink>
        <FooterLink liClass="mb-1" href="/">Change Network Password</FooterLink>
        <FooterLink liClass="mb-1" href="/">Agnel News Letter</FooterLink>
        <FooterLink liClass="mb-1" href="/">Bank/ NEFT Details</FooterLink>
        <FooterLink liClass="mb-1" href="/">Pay Us</FooterLink>
        <FooterLink liClass="mb-1" href="/">Mandatory Disclosure</FooterLink>
        <FooterLink liClass="mb-1" href="/">Online Grieviance/ Suggestion/ Feedback System</FooterLink>
        <FooterLink liClass="mb-1" href="/">MoU/ Collaboration/ Linkages</FooterLink>
      </FooterLinkGroup>
    </div>
    <div>
      <h2 class="mb-6 text-lg font-semibold uppercase text-gray-400">Library Quick Links</h2>
      <FooterLinkGroup ulClass="text-gray-300">
        <FooterLink liClass="mb-1" href="/">Fr. Agnel College Library Blogs</FooterLink>
        <FooterLink liClass="mb-1" href="/">ONline Library Catalog(Web OPAC)</FooterLink>
        <FooterLink liClass="mb-1" href="/">PG Student Resource Hub- PG Pathshala</FooterLink>
        <FooterLink liClass="mb-1" href="/">Rare Book Society of India</FooterLink>
        <FooterLink liClass="mb-1" href="/">IEEE Xplore</FooterLink>
        <FooterLink liClass="mb-1" href="/">ASME</FooterLink>
        <FooterLink liClass="mb-1" href="/">National DIgital Library</FooterLink>
        <FooterLink liClass="mb-1" href="/">Knimbus e-library</FooterLink>
        <FooterLink liClass="mb-1" href="/">QUestion Paper Archive</FooterLink>
        <FooterLink liClass="mb-1" >AICTE recommended e-books(free download)</FooterLink>
      </FooterLinkGroup>
    </div>
  </div>
  <div class="py-6 px-4 bg-gray-700 md:flex md:items-center md:justify-between">
    <FooterCopyright spanClass="text-lg text-gray-300 sm:text-center" href="/" by="TEAM CRCE_CONNECT™" />
    <div class="flex mt-4 space-x-6 sm:justify-center md:mt-0">
      <FooterIcon href="/">
        <FacebookSolid class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
      </FooterIcon>
      <FooterIcon href="/">
        <DiscordSolid class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
      </FooterIcon>
      <FooterIcon href="/">
        <TwitterSolid class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
      </FooterIcon>
      <FooterIcon href="/">
        <GithubSolid class="w-4 h-4 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
      </FooterIcon>
      <FooterIcon href="/">
        <!-- <Dribble /> -->
      </FooterIcon>
    </div>
  </div>
</Footer>