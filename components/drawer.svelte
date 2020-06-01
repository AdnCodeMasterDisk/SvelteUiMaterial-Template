<section>

  <div>

    <div class="drawer-container">
      <Drawer variant="modal" bind:this={myDrawer2} bind:open={myDrawer2Open}>
        <Header>
          <Title>Super Mail</Title>
          <Subtitle>It's the best fake mail app drawer.</Subtitle>
        </Header>
        <Content>
          <List>
            <Item href="javascript:void(0)" activated={active2 === 'Inbox'}>
              <Graphic class="material-icons" aria-hidden="true">inbox</Graphic>
              <Text>Inbox</Text>
            </Item>
            <Item href="javascript:void(0)" activated={active2 === 'Star'}>
              <Graphic class="material-icons" aria-hidden="true">star</Graphic>
              <Text>Star</Text>
            </Item>
            <Item href="javascript:void(0)" activated={active2 === 'Sent Mail'}>
              <Graphic class="material-icons" aria-hidden="true">send</Graphic>
              <Text>Sent Mail</Text>
            </Item>
            <Item href="javascript:void(0)" activated={active2 === 'Drafts'}>
              <Graphic class="material-icons" aria-hidden="true">drafts</Graphic>
              <Text>Drafts</Text>
            </Item>

            <Separator nav />
            <Subheader component={H6}>Labels</Subheader>
            <Item href="javascript:void(0)" activated={active2 === 'Family'}>
              <Graphic class="material-icons" aria-hidden="true">bookmark</Graphic>
              <Text>Family</Text>
            </Item>
            <Item href="javascript:void(0)" activated={active2 === 'Friends'}>
              <Graphic class="material-icons" aria-hidden="true">bookmark</Graphic>
              <Text>Friends</Text>
            </Item>
            <Item href="javascript:void(0)" activated={active2 === 'Work'}>
              <Graphic class="material-icons" aria-hidden="true">bookmark</Graphic>
              <Text>Work</Text>
            </Item>
          </List>
        </Content>
      </Drawer>

      <Scrim />
      <AppContent class="app-content">
        <main class="main-content">
          <Button on:click={() => myDrawer2Open = !myDrawer2Open}><Label>Toggle Drawer</Label></Button>
        </main>
      </AppContent>
    </div>
  </div>
</section>

<script>
  import Drawer, {AppContent, Content, Header, Title, Subtitle, Scrim} from '@smui/drawer';
  import Button, {Label} from '@smui/button';
  import List, {Item, Text, Graphic, Separator, Subheader} from '@smui/list';
  import H6 from '@smui/common/H6.svelte';

  let clicked = 'nothing yet';
  let myDrawer;
  let myDrawerOpen = false;
  let active = 'Gray Kittens';
  let myDrawer2;
  let myDrawer2Open = false;
  let active2 = 'Inbox';

</script>

<style>

</style>