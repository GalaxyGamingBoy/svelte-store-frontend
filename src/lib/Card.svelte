<script lang="ts">
    export let title = "";
    export let price = 0;
    export let stock = 0;
</script>

<div class="col-sm-6" style="width: 18rem; padding: 25px;">
    <div class="card">
        <div class="card-body">
            <h5 class="card-title">{title}</h5>
            <h6 class="card-subtitle mb-2 text-muted">
                Current Stock: {stock}
            </h6>
            <a href="#Cart" class="btn btn-primary">Buy for {price}€</a>
        </div>
    </div>
</div>
