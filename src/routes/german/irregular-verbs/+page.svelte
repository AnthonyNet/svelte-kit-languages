<script>
    import Navbar from '../../../components/navbar/Navbar.svelte';
    import Irregular from '../../../components/irregular/Irregular.svelte';
    import {VerbenData} from '../../../myData';


</script>

<Navbar />
<Irregular props={VerbenData} />