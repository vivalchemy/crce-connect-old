<script>
  import {
    Navbar,
    NavBrand,
    NavLi,
    NavUl,
    NavHamburger,
    Button,
    Dropdown,
    DropdownItem,
    DropdownDivider,
  } from "flowbite-svelte";
  import { ChevronDownOutline } from "flowbite-svelte-icons";
  import { page } from "$app/stores";
  $: activeUrl = $page.url.pathname;
</script>

<Navbar class="flex justify-center flex-wrap">
  <NavBrand href="/">
    <img src="crcelogo.jpg" class="h-16 sm:h-9" alt="FRCRCE LOGO" />
  </NavBrand>

  <div class="flex md:order-2">
    <Button class=" text-base" size="sm">Contact Us</Button>
    <NavHamburger menuClass="h-6 w-6 shrink-0" />
  </div>

  <NavUl {activeUrl} class="order-1">
    <NavLi class=" text-base" href="/">Home</NavLi>

    <NavLi class="cursor-pointer text-base ">
      About Us<ChevronDownOutline
        class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
      />
    </NavLi>
    <Dropdown class="w-44 z-20">
      <DropdownItem href="/">About CRCE</DropdownItem>
      <DropdownItem href="/docs/components/navbar"
        >From Director's Desk</DropdownItem
      >
      <DropdownItem href="/">Principal - Dr. Surendra Singh Rathod</DropdownItem
      >
      <DropdownItem href="/">Vision Mission</DropdownItem>
      <DropdownItem class="flex items-center justify-between"
        >Administration<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/">Trustees</DropdownItem>
          <DropdownItem href="/docs/components/navbar">Governance</DropdownItem>
          <DropdownItem href="/">Governing Council</DropdownItem>
          <DropdownItem href="/">Local Management Council</DropdownItem>
          <DropdownItem href="/">College Development Committee</DropdownItem>
          <DropdownItem href="/">Academic Cell</DropdownItem>
          <DropdownItem href="/">Strategic Development Plan</DropdownItem>
          <DropdownItem href="/">Service Rules</DropdownItem>
        </Dropdown>
      </DropdownItem>

      <DropdownItem class="flex flex-row items-center"
        >General Information<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/">AICTE Approvals</DropdownItem>
          <DropdownItem href="/docs/components/navbar">Core Values</DropdownItem
          >
          <DropdownItem href="/">Code of Conduct</DropdownItem>
          <DropdownItem href="/">Telephone Directory</DropdownItem>
          <DropdownItem href="/">Common Infrastructure</DropdownItem>
        </Dropdown>
      </DropdownItem>
      <DropdownItem href="/">Mandatory Disclosure</DropdownItem>
    </Dropdown>

    <!-- Drop down syntax -->
    <NavLi class="cursor-pointer text-base">
      Academics<ChevronDownOutline
        class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
      />
    </NavLi>
    <Dropdown class="w-44 z-20">
      <DropdownItem class=" flex justify-between items-center"
        >Examination<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/">About</DropdownItem>
          <DropdownItem href="/docs/components/navbar">Staff</DropdownItem>
          <DropdownItem href="/">Examination Process</DropdownItem>
        </Dropdown></DropdownItem
      >
      <DropdownItem class=" flex justify-between items-center"
        >Teaching learning process<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/">Teaching Learning Process</DropdownItem>
          <DropdownItem href="/docs/components/navbar">Lesson Plan</DropdownItem
          >
          <DropdownItem href="/">Syllabus</DropdownItem>
        </Dropdown>
      </DropdownItem>
      <DropdownItem class=" flex justify-between items-center"
        >NAAC<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/">NAAC 2018-19</DropdownItem>
          <DropdownItem href="/docs/components/navbar"
            >NAAC 2019-2020</DropdownItem
          >
          <DropdownItem href="/">NAAC 2020-2021</DropdownItem>
          <DropdownItem href="/">Best Practices</DropdownItem>
          <DropdownItem href="/">Institute Distinctiveness</DropdownItem>
          <DropdownItem href="/">NAAC Re-Assessment</DropdownItem>
        </Dropdown></DropdownItem
      >
      <DropdownItem class=" flex justify-between items-center"
        >Research And Development<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/">Overview</DropdownItem>
          <DropdownItem href="/docs/components/navbar"
            >Code of Ethics</DropdownItem
          >
          <DropdownItem href="/"
            >Publication, Patent, Funded Project</DropdownItem
          >
          <DropdownItem href="/">Research Centre Details</DropdownItem>
        </Dropdown></DropdownItem
      >
      <DropdownItem href="/">IQAC</DropdownItem>
      <DropdownItem class=" flex justify-between items-center"
        >Library<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/">Library Members</DropdownItem>
          <DropdownItem href="/docs/components/navbar"
            >Committee Members</DropdownItem
          >
          <DropdownItem href="/">Rules and Regulations</DropdownItem>
          <DropdownItem href="/">E-journals/E-books</DropdownItem>
          <DropdownItem href="/">Printed Journals</DropdownItem>
          <DropdownItem href="/">Services</DropdownItem>
        </Dropdown></DropdownItem
      >
      <DropdownItem href="/">AICTE recommended e-books | Free</DropdownItem>
      <DropdownItem class=" flex justify-between items-center"
        >OutReach Programmes<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/">IIIRSC-ISRO</DropdownItem>
        </Dropdown></DropdownItem
      >
      <DropdownItem href="/">List of MOU's</DropdownItem>
    </Dropdown>

    <NavLi class="cursor-pointer text-base">
      Department<ChevronDownOutline
        class="text-primary-800 w-3 h-3 ml-2  dark:text-white inline"
      />
    </NavLi>
    <Dropdown class="w-44 z-20">
      <DropdownItem href="/">Dashboard</DropdownItem>
      <DropdownItem href="/docs/components/navbar">Settings</DropdownItem>
      <DropdownItem href="/">Earnings</DropdownItem>
      <DropdownDivider />
      <DropdownItem href="/">Sign out</DropdownItem>
    </Dropdown>

    <NavLi class="cursor-pointer text-base">
      Students<ChevronDownOutline
        class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
      />
    </NavLi>
    <Dropdown class="w-44 z-20">
      <DropdownItem href="/">Dashboard</DropdownItem>
      <DropdownItem href="/docs/components/navbar">Settings</DropdownItem>
      <DropdownItem href="/">Earnings</DropdownItem>
      <DropdownDivider />
      <DropdownItem href="/">Sign out</DropdownItem>
    </Dropdown>

    <NavLi class="cursor-pointer text-base">
      Admission<ChevronDownOutline
        class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
      />
    </NavLi>
    <Dropdown class="w-44 z-20">
      <DropdownItem href="/">Dashboard</DropdownItem>
      <DropdownItem href="/docs/components/navbar">Settings</DropdownItem>
      <DropdownItem href="/">Earnings</DropdownItem>
      <DropdownDivider />
      <DropdownItem href="/">Sign out</DropdownItem>
    </Dropdown>
  </NavUl>
</Navbar>
