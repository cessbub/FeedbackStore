<script>
    import {FeedbackStore} from '../stores'

    $: count = $FeedbackStore.length
	$: average = $FeedbackStore.reduce((a, {rating}) => a + rating, 0) / $FeedbackStore.length
</script>

<div class="feedback-stats">
    <h4>{count} Reviews</h4>
    <h4>Ratings Average: {average}</h4>
</div>

<style>
    .feedback-stats{
        display: flex; /* put them in a row */
        justify-content: space-between;
        align-items: center;
    }
</style>