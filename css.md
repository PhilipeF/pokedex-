
        const colors = {
            fire: '#E4604D',
            grass: '#9DD465',
            electric: '#F9E45F',
            water: '#C3CD4A',
            ground: '#E4C967',
            rock: '#CABB7B',
            fairy: '#EEB2FA',
            poison: '#9F619D',
            bug: '#C5CF4A',
            dragon: '#857AF7',
            psychic: '#E56EAF',
            flying: '#80A4F9',
            fighting: '#9B5A48',
            normal: '#BAB8AB',
        }

        const variables = []
        const style = [];

        for (let key in colors) {

            variables.push(`--${key}: ${colors[key]};\n`);

            //console.log(key, colors[key])

            const css = `            
            .bg-${key} {
                background: linear-gradient(to top right, var(--${key}), var(--card-bg) 25%);
            }
            .${key} {
                background-color: var(--${key});
            } 
            `;

            style.push(css);
        }

        console.log(variables.join(''));
        console.log(style.join(''));