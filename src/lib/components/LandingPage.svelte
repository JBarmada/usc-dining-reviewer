<script>
    // Dummy data for testing
    const diningOptions = [
        { name: "Everybody's Kitchen", activityLevel: '63%', waitTime: '20 min.', logo : '/assets/everybodys_kitchen_logo.png' },
        { name: "Parkside", activityLevel: '91%', waitTime: '30 min.', logo: '/assets/parkside_logo.png' },
        { name: "USC Village Dining Hall", activityLevel: '27%', waitTime: '10 min.', logo: '/assets/usc_village_logo.png'}
    ];
</script>

<div class="inner-container">
    <div class="operating-hours">
        <div>Operating Hours (all dining halls):</div>
        <div>7:00AM - 10:00PM</div>
    </div>

    <div class="dining-options">
        {#each diningOptions as option}
        <div class="option">
            <div class="logo-container">
                <img class="logo" src={option.logo} alt="Dining Hall Logo" />
            </div>
            <div class="name">{option.name}</div>
            <div class="status-bar">
                <img src="assets/users.png" alt="Timer" class="icon" />
                <div class="bar-background">
                    <div class="activity-bar" style="width: {option.activityLevel};"></div>
                </div>
                <span class="activity-level">{option.activityLevel}</span>                
            </div>
            <div class="wait-time">
                <span class="wait-time">
                    <img src="assets/clock.png" alt="Timer" class="icon" />
                    <span class="wait-time-text">{option.waitTime}</span>   
                </span>
            </div>
        </div>
        {/each}
    </div>
</div>

<style>

    .name {
        margin: 1rem 0;
    }

    .wait-time {
        width: 100%;
        display: flex;
        align-items: center;
        gap: 1rem;
    }

    .wait-time-text {
        position: relative;
        right:50%;
        transform: translateX(50%);
    }

    .icon {
        width: 28px;
        height: 28px;
    }

    .logo-container {
        width: 100%;
    }

    .status-bar {
        width: 100%;
        display: flex;
        align-items: center;
        gap: 1rem;
    }

    .logo {
        height: 25vh;
    }

    .inner-container {
        padding: 1rem;
        background-color: #EDEDED;
        display: flex;
        align-items: center;
        flex-direction: column;
        gap: 1rem;
        height: 75vh;
    }

    .operating-hours {
        display: flex;
        align-items: center;
        flex-direction: column;
        margin: 7vh 0vh 2vh 0vh;
        color: black;
    }

    .dining-options {
        display: flex;
        flex-wrap: wrap;
        gap: 1rem;
        color: black;
    }

    .option {
        flex-basis: calc(25% - 1rem);
        padding: 1rem;
        text-align: center;
        display: flex;
        flex-direction: column;
    }

    .bar-background {
        background-color: white;
        height: 1vh;
        width: 20vh;
        border-radius: 5px;
        overflow: hidden;
    }

    .activity-bar {
        background-color: #d9534f;
        height: 100%;
        border-radius: 5px;
        left: 0;
        top: 0;
    }

    .wait-time {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
</style>
