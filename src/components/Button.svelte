<script>
    export let link
    export let buttonText
</script>

<a href="{link}">{buttonText}</a>

<style>
    a {
        display: inline-block; /* Ensures it behaves like a button */
        margin-top: 24px;
        padding: 16px 32px; /* Adjusted for better balance */
        background-color: #FF9900; /* Button background color */
        color: var(--dark); /* Text color */
        font-weight: 600; /* Bold text */
        text-align: center; /* Center text */
        text-decoration: none; /* Remove underline */
        border-radius: 5px; /* Rounded corners */
        transition: background-color 0.3s, transform 0.3s; /* Smooth transitions */
    }

    /* Add hover and active states for better interaction */
    a:hover {
        background-color: #e68a00; /* Darken on hover */
        transform: scale(1.05); /* Slightly enlarge */
    }

    a:active {
        background-color: #cc7a00; /* Darken further on active */
        transform: scale(0.98); /* Slightly shrink */
    }

    /* Optional: Adjust padding for smaller screens */
    @media (max-width: 600px) {
        a {
            padding: 12px 24px; /* Smaller padding for small screens */
            font-size: 0.875rem; /* Adjust font size */
        }
    }

</style>