<script lang="ts" context="module">
export async function preload(page) {
  const { name }: { name: string } = page.params;
  return { name: name.charAt(0).toUpperCase() + name.slice(1) };
}
</script>

<script lang="ts">
import TextCustom from "../../components/TextCustom.svelte";
import Room from "../../components/Room.svelte";
import RotatingAvatar from "../../components/RotatingAvatar.svelte";

export let name: string;
</script>

<svelte:head>
  <title>{name} a quelque chose à vous dire</title>
  <meta name="title" content="{name} a quelque chose à vous dire">
  <meta name="description"
        content="Hey ! C'est moi {name}. J'ai vraiment envie de te dire quelque chose... Mais je t'avoue que je ne sais pas trop comment m'y prendre. ❤😘😍💋">
  <meta property="og:title" content="{name} a quelque chose à vous dire">
  <meta property="og:description"
        content="Hey ! C'est moi {name}. J'ai vraiment envie de te dire quelque chose... Mais je t'avoue que je ne sais pas trop comment m'y prendre. ❤😘😍💋">
  <meta property="twitter:title" content="{name} a quelque chose à vous dire">
  <meta property="twitter:description"
        content="Hey ! C'est moi {name}. J'ai vraiment envie de te dire quelque chose... Mais je t'avoue que je ne sais pas trop comment m'y prendre. ❤😘😍💋">
</svelte:head>

<Room>
  <TextCustom color="#00F7FF" x={1} y={1} size="5rem" move="-2rem">{name} vous a Codysé !</TextCustom>
  <TextCustom color="#77FF00" x={0.5} y={0.5} size="2rem" move="2rem">Gros bisous sur tes joues mon loulou</TextCustom>
  <RotatingAvatar/>
</Room>



