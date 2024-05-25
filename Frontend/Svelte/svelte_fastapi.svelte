<script>
let potat=2
let tomat=4

//sending data
async function sendData(){

    const payload = {potat, tomat}; //payload the 
    try {
        // HACK: await fetch (url, {method: val, headers: val, body: val})
        const response = await fetch('http://fastapiLink.com/this_endpoint', {
            methods: 'POST',
            headers: { 'Conetent-Type : 'application/json'},
            body: JSON.stringify(payload)

        });

        if (!response.ok) { throw new Error('Not Okay')}

        const jsonresponse = await response.json() // .josn() to get just json info, no metadata

    } catch (error) {
        console.error('error',error)
    }
}

</script>