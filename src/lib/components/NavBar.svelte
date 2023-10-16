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
      <DropdownItem href="/aboutus/aboutCrce">About CRCE</DropdownItem>
      <DropdownItem href="/aboutus/directorsDesk"
        >From Director's Desk</DropdownItem
      >
      <DropdownItem href="/aboutus/principal"
        >Principal - Dr. Surendra Singh Rathod</DropdownItem
      >
      <DropdownItem href="/aboutus/visionAndMission"
        >Vision Mission</DropdownItem
      >
      <DropdownItem class="flex items-center justify-between"
        >Administration<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/aboutus/administration/trustees"
            >Trustees</DropdownItem
          >
          <DropdownItem href="/aboutus/administration/governingcouncil"
            >Governance</DropdownItem
          >
          <DropdownItem href="/aboutus/administration/governingcouncil"
            >Governing Council</DropdownItem
          >
          <DropdownItem href="/aboutus/administration/localManagement"
            >Local Management Council</DropdownItem
          >
          <DropdownItem
            href="/aboutus/administration/collageDevolopementCommitee"
            >College Development Committee</DropdownItem
          >
          <DropdownItem href="/aboutus/administration/academicCell"
            >Academic Cell</DropdownItem
          >
          <DropdownItem
            href="/aboutus/administration/stratergicDevolopementPlan"
            >Strategic Development Plan</DropdownItem
          >
          <DropdownItem href="/aboutus/administration/"
            >Service Rules</DropdownItem
          >
        </Dropdown>
      </DropdownItem>

      <DropdownItem class="flex flex-row items-center"
        >General Information<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/generalinfo/AITCEapprovals"
            >AICTE Approvals</DropdownItem
          >
          <DropdownItem href="/generalinfo/corevalues">Core Values</DropdownItem
          >
          <DropdownItem href="/generalinfo/codeofconduct"
            >Code of Conduct</DropdownItem
          >
          <DropdownItem href="/">Telephone Directory</DropdownItem>
          <DropdownItem href="/generalinfo/commoninfra"
            >Common Infrastructure</DropdownItem
          >
        </Dropdown>
      </DropdownItem>
      <DropdownItem href="/ManditoryDisclosure"
        >Mandatory Disclosure</DropdownItem
      >
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
          <DropdownItem href="/Academics/examiantion/about">About</DropdownItem>
          <DropdownItem href="/Academics/examiantion/staff">Staff</DropdownItem>
          <DropdownItem href="/Academics/examiantion/examprocess"
            >Examination Process</DropdownItem
          >
        </Dropdown></DropdownItem
      >
      <DropdownItem class=" flex justify-between items-center"
        >Teaching learning process<ChevronDownOutline
          class="w-3 h-3 ml-2 text-primary-800 dark:text-white inline"
        />
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/Academics/teachingProcess">Teaching Learning Process</DropdownItem>
          <DropdownItem href="/Academics/teachingProcess/lessonplan">Lesson Plan</DropdownItem
          >
          <DropdownItem href="/Academics/teachingProcess/teachinglearning">Syllabus</DropdownItem>
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
          <DropdownItem href="/Academics/RandD/overview">Overview</DropdownItem>
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
