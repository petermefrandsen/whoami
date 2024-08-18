<script>
    let firstname = 'Peter';
    let middlename = 'Meyer Elphick';
    let lastname = 'Frandsen';
    let fullname = `${firstname} ${middlename} ${lastname}`;
    //calculate age from specific date 1991 september 2,
    let birthDate = new Date(1991, 9-1, 2); // September is month 8 (zero-based index)
    let currentDate = new Date();
    let age = currentDate.getFullYear() - birthDate.getFullYear();
    if (currentDate.getMonth() < birthDate.getMonth() || (currentDate.getMonth() === birthDate.getMonth() && currentDate.getDate() < birthDate.getDate())) {
        age--;
    }

    let images = [
        'images/taekwondo-kick.gif',
        'images/house-extension.png',
        'image3.jpg'
    ];
    let currentImage = 0;

    function rotateImages() {
        setInterval(() => {
            currentImage = (currentImage + 1) % images.length;
        }, 5000);
    }

    rotateImages();
</script>

<div class="container">
    <div class="header">
        <h1>WhoAmI</h1>
    </div>
    <div class="full-width">full width</div>
    <div class="two-columns">
        <div>
            <h2>Basics</h2>
            <p>Name: {fullname}</p>
            <p>Age: {age}</p>
        </div>
        <div>right 50%</div>
    </div>
    <div class="full-width">
        <div class="experience">
            <h2>Experience</h2>
            <ul>
                <li>
                    <h3>Vestas</h3>
                    <p>Chapter Lead, Feb 2024 - Present</p>
                </li>
                <li>
                    <h3>Consultant, Inspari A/S</h3>
                    <p>May 2023 - Jan 2024</p>
                    <p>Principal Cloud Solution Architect</p>
                    <p>Various tasks related to customer implementations as well as product development for the Inspari reporting product; Actify.</p>
                </li>
                <li>
                    <h3>Vestas</h3>
                    <p>Platform Owner, Aug 2022 - Apr 2023</p>
                    <p>In Vestas, I have been Platform Owner of the Developer Observability Platform and the Data Streaming Platform and Developer Experience Platform.</p>
                    <p>Cloud Architect, Oct 2021 - Aug 2022</p>
                    <p>As Cloud Architect, I worked on implementing our Data Streaming Platform and with Technical Business Engagement to bridge the gap between software developers and infrastructure developers.</p>
                </li>
                <li>
                    <h3>Norlys</h3>
                    <p>Lead Software Developer, Jan 2021 - Sep 2021</p>
                    <p>As Lead Software Developer at Norlys I have worked with developing and maintaining solutions around Master Data and other company related data as well as ensuring the quality of the developed solutions and the progress within the ongoing project.</p>
                    <p>Software Developer, Apr 2020 - Jan 2021</p>
                    <p>As a software developer, I worked with developing solutions regarding the provisioning system that ensures customers are able to get internet.</p>
                </li>
                <li>
                    <h3>MHI Vestas Offshore Wind (now Vestas)</h3>
                    <p>Software Developer, Jan 2019 - Mar 2020</p>
                    <p>As a software developer, I worked with developing monitoring software for energy production and model prediction results from wind turbines.</p>
                </li>
                <li>
                    <h3>Eniig (now Norlys)</h3>
                    <p>Quality Manager, Jun 2017 - Dec 2018</p>
                    <p>As Quality Manager I had to ensure that my colleague's work lived up to the company and legislation standards without affecting the performance of the work.</p>
                    <p>Energy Consultant, May 2016 - May 2017</p>
                    <p>As Energy Consultant my main task was to complete projects and do quality assurance of documentation made by other parties.</p>
                </li>
            </ul>
        </div>

        <div class="education">
            <h2>Education</h2>
            <ul>
                <li>
                    <h3>Copenhagen Business Academy - 2018-2020</h3>
                    <p>Academy Profession, Information Technology - Development</p>
                </li>
                <li>
                    <h3>M.Sc. @ Aarhus University - 2014-2016</h3>
                    <p>Master's degree, Civil and Architectural Engineering - Integrated Energy Design</p>
                </li>
                <li>
                    <h3>B.Eng. @ Aarhus University - 2010-2014</h3>
                    <p>Bachelor of Engineering (B.Eng.), Architectural Engineering - Energy and Indoor Climate</p>
                </li>
            </ul>
        </div>
    </div>
    <div class="full-width">
        <div class="image-carousel">
            <img src={images[currentImage]} alt="Image" />
        </div>
    </div>
    <div class="footer">footer</div>
</div>


<style>
@media (min-width: 1024px) {
    .container {
        margin-left: calc((100vw - 1024px) / 2);
        margin-right: calc((100vw - 1024px) / 2);
        max-width: 1024px;
    }
}

.container {
    display: flex;
    flex-direction: column;
    height: 100vh;
}

.header,
.footer {
    background-color: lightgray;
    padding: 10px;
}

.full-width {
    background-color: lightblue;
    padding: 10px;
}

.two-columns {
    display: flex;
    flex-direction: row;
}

.two-columns > div {
    flex: 1;
    padding: 10px;
    background-color: lightgreen;
}

.image-carousel {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 10px;
    background-color: lightyellow;
    height: 500px;
}

.image-carousel img {
    max-width: 100%;
    max-height: 100%;
    width: auto;
    height: auto;
    margin-bottom: 10px;
}

</style>