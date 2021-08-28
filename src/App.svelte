<script lang="ts">
  import {
    Collapse,
    Container,
    Navbar,
    NavbarToggler,
    NavbarBrand,
    Nav,
    NavItem,
    NavLink,
    Dropdown,
    DropdownToggle,
    DropdownMenu,
    DropdownItem
  } from 'sveltestrap';

  let isOpen = false;

  function handleUpdate(event) {
    isOpen = event.detail.isOpen;
  }
</script>

<header>
    <Navbar color="primary" dark expand="md" class="m-auto">
      <NavbarBrand href="/">Svelte + Bootstrap 5</NavbarBrand>
      <NavbarToggler on:click={() => (isOpen = !isOpen)} />
      <Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
        <Nav class="ms-auto h5" navbar>
          <NavItem class="me-2">
            <NavLink href="https://github.com/jmmaranan/sveltestrap-starter">Github</NavLink>
          </NavItem>
        </Nav>
      </Collapse>
    </Navbar>
</header>

