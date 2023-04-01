<script>
    import Navbar from '../../../components/navbar/Navbar.svelte';
    import Irregular from '../../../components/irregular/Irregular.svelte';
    import {VerbenData} from '../../../myData';

	const sortData = () =>{
const random = Math.floor(Math.random() * VerbenData.length);
const data = VerbenData[random];
return data;
}
</script>

<Navbar />
<Irregular sortData={sortData()} />