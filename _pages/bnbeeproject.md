---
layout: page
title: The BnBee Project
permalink: /bnbeeproject/
description: 
nav: true
nav_order: 3
---

<style>
.buzz-fact {
    background: linear-gradient(45deg, #fff3e0, #ffe0b2);
    border-left: 5px solid #ff9800;
    padding: 20px;
    margin: 30px 0;
    border-radius: 10px;
    position: relative;
}

.buzz-fact::before {
    content: '🐝';
    position: absolute;
    left: -15px;
    top: -5px;
    font-size: 30px;
    background: white;
    border-radius: 50%;
    padding: 5px;
}

.buzz-fact h4 {
    color: #e67e22;
    font-size: 1.3rem;
    margin-bottom: 10px;
    font-weight: bold;
}

.workshop-section {
    background: #f8f9fa;
    border-radius: 15px;
    padding: 30px;
    margin: 30px 0;
    border: 2px solid #007bff;
}

.workshop-section h3 {
    color: #007bff;
    font-size: 1.8rem;
    margin-bottom: 20px;
    text-align: center;
    border-bottom: 3px solid #007bff;
    padding-bottom: 10px;
}

.activity-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 25px;
    margin: 30px 0;
}

.activity-card {
    background: linear-gradient(135deg, #e3f2fd, #bbdefb);
    color: #1565c0;
    padding: 25px;
    border-radius: 15px;
    text-align: center;
    border: 2px solid #2196f3;
    transition: transform 0.3s ease;
}

.activity-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 25px rgba(33, 150, 243, 0.2);
}

.activity-card h4 {
    font-size: 1.4rem;
    margin-bottom: 15px;
    font-weight: bold;
}

.activity-emoji {
    font-size: 3rem;
    display: block;
    margin-bottom: 15px;
}

.instructions-box {
    background: #e8f5e8;
    border-radius: 12px;
    padding: 25px;
    margin: 20px 0;
    border: 2px dashed #28a745;
}

.instructions-box h4 {
    color: #28a745;
    font-size: 1.3rem;
    margin-bottom: 15px;
    font-weight: bold;
}

.step {
    display: flex;
    align-items: flex-start;
    margin: 15px 0;
    padding: 15px;
    background: white;
    border-radius: 8px;
    border-left: 4px solid #28a745;
}

.step-number {
    background: #28a745;
    color: white;
    width: 30px;
    height: 30px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    margin-right: 15px;
    flex-shrink: 0;
    font-size: 1rem;
}

.fun-facts-box {
    background: linear-gradient(135deg, #f8d7da, #f5c6cb);
    color: #721c24;
    border-radius: 15px;
    padding: 30px;
    margin: 30px 0;
    text-align: center;
    border: 2px solid #dc3545;
}

.fun-facts-box h4 {
    font-size: 1.8rem;
    margin-bottom: 20px;
    font-weight: bold;
}

.fact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin-top: 25px;
}

.fact-item {
    background: rgba(255,255,255,0.7);
    padding: 20px;
    border-radius: 10px;
    border: 1px solid #dc3545;
}

.fact-emoji {
    font-size: 2.5rem;
    margin-bottom: 10px;
    display: block;
}

.conservation-message {
    background: linear-gradient(135deg, #d4edda, #c3e6cb);
    color: #155724;
    border-radius: 20px;
    padding: 40px;
    text-align: center;
    margin: 40px 0;
    position: relative;
    border: 3px solid #28a745;
}

.conservation-message::before {
    content: '🌍💚🐝';
    position: absolute;
    top: -20px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 30px;
    background: white;
    padding: 10px 20px;
    border-radius: 25px;
    border: 2px solid #28a745;
}

.conservation-message h4 {
    font-size: 1.8rem;
    margin-bottom: 20px;
    margin-top: 20px;
    font-weight: bold;
}

.species-list {
    background: #f8f9fa;
    border-radius: 12px;
    padding: 25px;
    margin: 25px 0;
    border: 2px solid #6f42c1;
}

.species-list h4 {
    color: #6f42c1;
    font-size: 1.4rem;
    margin-bottom: 15px;
    text-align: center;
    font-weight: bold;
}

.species-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
}

.species-tag {
    background: linear-gradient(45deg, #9c88ff, #6f42c1);
    color: white;
    padding: 8px 15px;
    border-radius: 20px;
    font-size: 0.9rem;
    font-weight: bold;
}

@media (max-width: 768px) {
    .activity-grid, .fact-grid {
        grid-template-columns: 1fr;
    }
    
    .step {
        flex-direction: column;
        text-align: center;
    }
    
    .step-number {
        margin-right: 0;
        margin-bottom: 10px;
    }
}
</style>

<div class="row justify-content-center mt-3">
    <div class="col-12">
        {% include figure.liquid loading="eager" path="assets/img/bnbeeproject.jpg" title="The BnBee Project: Hotels for Pollinators" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<p>
The BnBee Project is all about creating safe, welcoming homes for solitary native bees. These bees are essential pollinators in our gardens, schools, and natural ecosystems, but many species struggle to find suitable nesting sites due to habitat loss.
</p>


<div class="buzz-fact">
    <h4>Did You Know?</h4>
    <p>Australia has over <strong>2,000 species</strong> of native bees! Most of them are solitary bees that don't live in colonies like honey bees. They're super important pollinators that help our plants grow and produce food!</p>
</div>

<div class="workshop-section">
    <h3>Workshops</h3>
       
    <div class="activity-grid">
        <div class="activity-card">
            <span class="activity-emoji">🐝</span>
            <h4>Build Bee Hotels</h4>
            <p>Create cozy homes for native bees using natural materials like bamboo. These hotels give solitary bees safe places to lay their eggs!</p>
        </div>
        
        <div class="activity-card">
            <span class="activity-emoji">🌱</span>
            <h4>Make Native Seed Bombs</h4>
            <p>Mix clay, soil, and native flower seeds to create "seed bombs" that will grow into beautiful bee-friendly gardens!</p>
        </div>
    </div>
</div>

<div class="workshop-section">
    <h3>How to Use Your Native Bee Hotel</h3>
       
    <div class="instructions-box">
      
        <div class="step">
            <div class="step-number">1</div>
            <div>
                <strong>Choose a sheltered, dry spot under cover</strong><br>
                Find a location like a verandah or under a tree branch that protects the hotel from rain and harsh weather.
            </div>
        </div>
        <div class="step">
            <div class="step-number">2</div>
            <div>
                <strong>Position 1-2 meters above ground, facing east or north-east</strong><br>
                This height keeps the hotel safe from ground predators and the eastern orientation provides gentle morning sun.
            </div>
        </div>
        <div class="step">
            <div class="step-number">3</div>
            <div>
                <strong>Make sure the hotel is secured tightly</strong><br>
                The structure shouldn't wobble or swing in the wind, as this can disturb nesting bees.
            </div>
        </div>
        <div class="step">
            <div class="step-number">4</div>
            <div>
                <strong>Do not attempt to open, shake, or disassemble the hotel</strong><br>
                Once installed, leave it undisturbed so the bees can nest peacefully and complete their life cycle.
            </div>
        </div>
    </div>
</div>

<div class="workshop-section">
    <h3>How to Use Your Native Flower Seed Bomb</h3>
      
    <div class="instructions-box">
            <div class="step">
            <div class="step-number">1</div>
            <div>
                <strong>Choose a bare soil spot in your garden or use a pot</strong><br>
                Avoid planting in established grasses so seedlings don't have to compete for space and nutrients.
            </div>
        </div>
        <div class="step">
            <div class="step-number">2</div>
            <div>
                <strong>Place the seed bomb on the soil surface or press in lightly</strong><br>
                Don't bury it deeply - the seeds need access to light and air to germinate properly.
            </div>
        </div>
        <div class="step">
            <div class="step-number">3</div>
            <div>
                <strong>Water well and don't let dry out once germinating</strong><br>
                Keep the soil consistently moist but not waterlogged during the germination period.
            </div>
        </div>
        <div class="step">
            <div class="step-number">4</div>
            <div>
                <strong>Water well if steady rainfall is not forecast</strong><br>
                Until plants are established, try to allow soil to semi-dry between waterings to encourage deep root growth.
            </div>
        </div>
        <div class="step">
            <div class="step-number">5</div>
            <div>
                <strong>Best used within 6 months</strong><br>
                Seed viability decreases over time, so plant your seed bombs relatively soon after receiving them.
            </div>
        </div>
    </div>
    
    <div class="species-list">
        <h4>🌸 Native Flower Species in Your Seed Bomb</h4>
        <div class="species-tags">
            <span class="species-tag">Golden Cluster Everlasting</span>
            <span class="species-tag">Swan River Daisy</span>
            <span class="species-tag">Pink & White Everlasting</span>
            <span class="species-tag">Daisy coloured mix</span>
            <span class="species-tag">Dwarf Strawflower</span>
            <span class="species-tag">Billy Buttons</span>
            <span class="species-tag">Red & Yellow Kangaroo Paw</span>
            <span class="species-tag">Blue Lace Flower</span>
            <span class="species-tag">Native Wisteria</span>
            <span class="species-tag">Coral Creeper</span>
            <span class="species-tag">Ashburton Pea</span>
        </div>
    </div>
</div>

<div class="fun-facts-box">
    <h4>🐝 Amazing Native Bee Facts!</h4>
    <div class="fact-grid">
        <div class="fact-item">
            <span class="fact-emoji">🏠</span>
            <h5>Tiny Architects</h5>
            <p>Native bees build amazing nests in hollow stems, holes in wood, or even underground burrows!</p>
        </div>
        <div class="fact-item">
            <span class="fact-emoji">🌺</span>
            <h5>Buzz Pollination</h5>
            <p>Some native bees are "buzz pollinators" - they grab flowers and vibrate their flight muscles to shake out the pollen!</p>
        </div>
        <div class="fact-item">
            <span class="fact-emoji">🌈</span>
            <h5>Rainbow Colors</h5>
            <p>Native bees come in amazing colors - metallic green, bright blue, fuzzy orange, and striped black and white!</p>
        </div>
    </div>
</div>

<div class="conservation-message">
    <h4>Why Native Bees Need Our Help</h4>
    <p>Native bees are losing their homes due to habitat loss, urban development, and changes in land use. By building bee hotels and planting native flowers, we create safe spaces for these amazing pollinators.</p>
    <p>When we support native bees, we support biodiversity, help maintain healthy plant communities, and contribute to the resilience of our natural environment.</p>
</div>

<div class="row mt-4">
    <div class="col-md-6">
        <h4>🔗 Learn More</h4>
        <ul>
            <li><a href="https://www.wheenbeefoundation.org.au/about-bees-pollination/australian-native-bees/">Australian Native Bees - Wheen Bee Foundation</a></li>
            <li><a href="https://www.krg.nsw.gov.au/Environment/Your-local-environment/Wildlife/Living-with-wildlife/Bee-hotels">Bee Hotels - Ku-ring-gai Council</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <h4>📞 Workshop Bookings</h4>
        <p>Interested in bringing the BnBee Project to your school? My contact details can be found on the About page.
    </div>
</div>
