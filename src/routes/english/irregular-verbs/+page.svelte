<script>
    import Navbar from '../../../components/navbar/Navbar.svelte';
    import Irregular from '../../../components/irregular/Irregular.svelte';
    import {IrregularVerbs} from '../../../myData';

const sortData = () =>{
const random = Math.floor(Math.random() * IrregularVerbs.length);
const data = IrregularVerbs[random];
return data;
}

console.log(sortData());

</script>

<Navbar />
<Irregular myData={sortData()} />