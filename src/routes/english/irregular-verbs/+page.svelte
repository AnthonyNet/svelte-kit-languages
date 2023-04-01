<script>
    import Navbar from '../../../components/navbar/Navbar.svelte';
    import Irregular from '../../../components/irregular/Irregular.svelte';
    import {IrregularVerbs} from '../../../myData';
</script>

<Navbar />
<Irregular props={IrregularVerbs}/>