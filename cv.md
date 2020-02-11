# Resume for vacancy Junior developer

1. **Kruglov Dmitrii**
2. Contact Info:
* e-mail: krudda@yandex.ru
* phone: +7 920 254 08 80
3. I am interested in the opportunity to change the direction of professional activity, and I would like to get a job as a junior front-end developer.
To gain knowledge, I graduated from six-month offline continuing education courses at Lobachevsky University (Nizhny Novgorod), specializing in web development. The training involved HTML, CSS, PHP, JS. In addition, I attended offline courses on React from the Nizhny Novgorod IT-company Lad. I'm learning JS and ReactNativ myself.

My professional competencies include a lot of Fin-tech experience: 
- building an architecture for organizing electronic payments, interacting with banks. 
- I know the internal processes of Russian credit organizations, the principles of operation of international payment systems and the instant payment system of the Central Bank of Russia (SBP). 
- I am familiar with the relevant legislation governing banking and accepting payments, as well as with the regulatory framework of the Bank Of Russia.
- In addition, I devoted a lot of time to building relationships with banks and recipients of funds.

Among my personal qualities, I can note the ability to compromise in business negotiations, maintain calm in stressful working situations, quickly understand complex issues, and lead a team.
I love and know how to get knowledge.

4. Skills:
* JS at a basic level, using ES6. 
* know and use HTML5 and CSS3 sufficiently.
* basics of PHP and work with the database (SQL).
* basics of React, ReactNative.
5. Sample code for an example of a component for a mobile application (ReactNative):
```javascript
import React , {useState} from 'react';
import {ScrollView, ImageBackground,  StyleSheet, TouchableOpacity} from 'react-native';
import NoteBox from '../noteBox/index';
import THEME from '../../values/theme';
import RoundButton from '../roundButton';
import screenNames from '../../navigation/screenNames';
import { connect } from 'react-redux';
import actions from '../../actions/actions';
 
const GeneralScreen =  (props) => {
        // hooks
        const [editIndex, setEditIndex] = useState(false);
        const setEdit = (index) => {setEditIndex(index)};
        const unsetEdit = () => {setEditIndex(false)};

        //methods
        const goToEditor = ()=> {props.navigation.push(screenNames.editor)}
        const renderNotes = () => {
                return props.data.notes.map( (elem, index) => {
                        return (
                                <TouchableOpacity 
                                        key = {index} 
                                        onLongPress = {()=> {setEdit(index)}} 
                                        onPress = {unsetEdit}
                                        activeOpacity = {1}
                                >
                                        <NoteBox 
                                                header = {elem.header} 
                                                content = {elem.content}
                                                editMode = {index === editIndex}
                                        />
                                </TouchableOpacity>
                                );
                });
        }
        // render
        return (
                <ImageBackground 
                        style = {styles.wrapper}
                        source={THEME.generalScreen.background}
                        resizeMode={'contain'}
                        // blurRadius={15}
                        >
                        <ScrollView>
                                {renderNotes()}
                        </ScrollView>
                <TouchableOpacity 
                        activeOpacity={0.5}
                        style = {styles.activeButton}
                        onPress={goToEditor}>
                        
                        <RoundButton img={THEME.actionButton.img}/>
                        {
                                editIndex !== false && (
                                        <RoundButton img={THEME.actionButton.img} />
                                )
                        }
                </TouchableOpacity>
                </ImageBackground>)
}
const styles = StyleSheet.create ({
        wrapper: {
                flex: 1,
                paddingTop: THEME.generalScreen.paddingTop,
        },
        activeButton: {
                position: 'absolute',
                bottom: 30,
                right: 30
        }
})

export default connect( (store) => {
        return {
                data: store.data
        }
}, actions)(GeneralScreen);
```

6. Experience:

7. Education:
* Lobachevsky University (Nizhny Novgorod), specializing in web development (HTML, CSS, PHP, JS)
* Online courses Udemy: JavaScript, React, ReactNative
* offline courses from IT company Lad on React

8. My English can hardly be called "Pre-intermediate".
I can understand, write and talk on everyday topics. In foreign trips I can explain my wishes.
I read with the dictionary.

