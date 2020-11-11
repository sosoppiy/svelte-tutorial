<script>
    import Router from 'svelte-spa-router'
    import Main from './Main.svelte';

    // introduction
    import Basics from "./introduction/Basics.svelte";
    import AddingData from "./introduction/AddingData.svelte";
    import DynamicAttributes from "./introduction/DynamicAttributes.svelte";
    import Styling from "./introduction/Styling.svelte";
    import NestedComponents from "./introduction/NestedComponents.svelte";
    import HtmlTags from "./introduction/HtmlTags.svelte";

    // reactive
    import Assignments from "./reactive/Assignments.svelte";
    import Declarations from "./reactive/Declarations.svelte";
    import ReactiveStatements from "./reactive/ReactiveStatements.svelte";
    import UpdatingArraysAndbjects from "./reactive/UpdatingArraysAndbjects.svelte";
      
    const routes = {
      '/': Main,
      '/introduction/basics': Basics,
      "/introduction/adding-data": AddingData,
      "/introduction/dynamic-attributes": DynamicAttributes,
      "/introduction/styling": Styling,
      "/introduction/nested-components": NestedComponents,
      "/introduction/html-tags" :HtmlTags,
      "/reactive/assignments" :Assignments,
      "/reactive/declarations" :Declarations,
      "/reactive/reactive-statements" :ReactiveStatements,
      "/reactive/updating-arrays-and-objects" :UpdatingArraysAndbjects,
      
    };
  </script>
  
  <main>
    <Router routes={routes}></Router>
  </main>