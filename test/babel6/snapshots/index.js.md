# Snapshot report for `test/babel6/index.js`

The actual snapshot is saved in `index.js.snap`.

Generated by [AVA](https://ava.li).

## generates source maps

> Snapshot 1

    `import _JSXStyle from 'styled-jsx/style';␊
    export default (() => <div className={"jsx-2743241663"}>␊
        <p className={"jsx-2743241663"}>test</p>␊
        <p className={"jsx-2743241663"}>woot</p>␊
        <_JSXStyle id={"2743241663"}>{"p.jsx-2743241663{color:red;}\\n/*# sourceMappingURL=data:application/json;charset=utf-8;base64,eyJ2ZXJzaW9uIjozLCJzb3VyY2VzIjpbInNvdXJjZS1tYXBzLmpzIl0sIm5hbWVzIjpbXSwibWFwcGluZ3MiOiJBQUlnQixBQUNjLFVBQUMiLCJmaWxlIjoic291cmNlLW1hcHMuanMiLCJzb3VyY2VzQ29udGVudCI6WyJleHBvcnQgZGVmYXVsdCAoKSA9PiAoXG4gIDxkaXY+XG4gICAgPHA+dGVzdDwvcD5cbiAgICA8cD53b290PC9wPlxuICAgIDxzdHlsZSBqc3g+eydwIHsgY29sb3I6IHJlZCB9J308L3N0eWxlPlxuICA8L2Rpdj5cbilcbiJdfQ== */\\n/*@ sourceURL=source-maps.js */"}</_JSXStyle>␊
      </div>);`

## ignores when attribute is absent

> Snapshot 1

    `const a = () => <div>␊
        <p>hi</p>␊
        <style>{'woot'}</style>␊
      </div>;`

## ignores whitespace around expression container

> Snapshot 1

    `import _JSXStyle from 'styled-jsx/style';␊
    export default (() => <div className={"jsx-2743241663"}>␊
        <p className={"jsx-2743241663"}>test</p>␊
        <p className={"jsx-2743241663"}>woot</p>␊
        <p className={"jsx-2743241663"}>woot</p>␊
        <_JSXStyle id={"2743241663"}>{"p.jsx-2743241663{color:red;}"}</_JSXStyle>␊
      </div>);`

## mixed global and scoped

> Snapshot 1

    `import _JSXStyle from 'styled-jsx/style';␊
    const Test = () => <_JSXStyle id={"2743241663"}>{"p{color:red;}"}</_JSXStyle>;␊
    ␊
    export default (() => <div className={"jsx-2673076688"}>␊
        <p className={"jsx-2673076688"}>test</p>␊
        <_JSXStyle id={"4269072806"}>{"body{background:red;}"}</_JSXStyle>␊
        <_JSXStyle id={"2743241663"}>{"p.jsx-2673076688{color:red;}"}</_JSXStyle>␊
      </div>);`

## should have different jsx ids

> Snapshot 1

    `import _JSXStyle from 'styled-jsx/style';␊
    const color = 'red';␊
    const otherColor = 'green';␊
    ␊
    const A = () => <div className={"jsx-57381496"}>␊
        <p className={"jsx-57381496"}>test</p>␊
        <_JSXStyle id={"57381496"}>{`p.jsx-57381496{color:${color};}`}</_JSXStyle>␊
      </div>;␊
    ␊
    const B = () => <div className={"jsx-3099245642"}>␊
        <p className={"jsx-3099245642"}>test</p>␊
        <_JSXStyle id={"3099245642"}>{`p.jsx-3099245642{color:${otherColor};}`}</_JSXStyle>␊
      </div>;␊
    ␊
    export default (() => <div>␊
        <A />␊
        <B />␊
      </div>);`

## should not add the data-jsx attribute to components instances

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    const Test = () => <div className={"jsx-2529315885"}>␊
        <span className={"jsx-2529315885"}>test</span>␊
        <Component />␊
        <_JSXStyle id={"2529315885"}>{"span.jsx-2529315885{color:red;}"}</_JSXStyle>␊
      </div>;`

## works with class

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    export default class {␊
    ␊
      render() {␊
        return <div className={"jsx-2101845350"}>␊
            <p className={"jsx-2101845350"}>test</p>␊
            <_JSXStyle id={"2101845350"}>{"p.jsx-2101845350{color:red;}"}</_JSXStyle>␊
          </div>;␊
      }␊
    ␊
    }`

## works with css tagged template literals in the same file

> Snapshot 1

    `import _JSXStyle from 'styled-jsx/style';␊
    ␊
    ␊
    export default (({ children }) => <div className={`jsx-${styles.__hash}`}>␊
        <p className={`jsx-${styles.__hash}`}>{children}</p>␊
        <_JSXStyle id={styles.__hash}>{styles}</_JSXStyle>␊
      </div>);␊
    ␊
    const styles = new String('p.jsx-2587355013{color:red;}');␊
    ␊
    styles.__hash = '2587355013';␊
    class Test extends React.Component {␊
      render() {␊
        return <div className={`jsx-${styles.__hash}`}>␊
            <p className={`jsx-${styles.__hash}`}>{this.props.children}</p>␊
            <_JSXStyle id={styles.__hash}>{styles}</_JSXStyle>␊
          </div>;␊
      }␊
    }`

## works with dynamic element

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    export default (({ level = 1 }) => {␊
      const Element = `h${level}`;␊
    ␊
      return <Element className={"jsx-1253978709" + " " + "root"}>␊
          <p className={"jsx-1253978709"}>dynamic element</p>␊
          <_JSXStyle id={"1253978709"}>{".root.jsx-1253978709{background:red;}"}</_JSXStyle>␊
        </Element>;␊
    });␊
    ␊
    export const TestLowerCase = ({ level = 1 }) => {␊
      const element = `h${level}`;␊
    ␊
      return <element className={"jsx-1253978709" + " " + "root"}>␊
          <p className={"jsx-1253978709"}>dynamic element</p>␊
          <_JSXStyle id={"1253978709"}>{".root.jsx-1253978709{background:red;}"}</_JSXStyle>␊
        </element>;␊
    };␊
    ␊
    const Element2 = 'div';␊
    export const Test2 = () => {␊
      return <Element2 className="root">␊
          <p className={"jsx-1253978709"}>dynamic element</p>␊
          <_JSXStyle id={"1253978709"}>{".root.jsx-1253978709{background:red;}"}</_JSXStyle>␊
        </Element2>;␊
    };`

## works with dynamic element in class

> Snapshot 1

    `import _JSXStyle from 'styled-jsx/style';␊
    export default class {␊
      render() {␊
        const Element = 'div';␊
    ␊
        return <Element className={'jsx-1800172487' + ' ' + 'root'}>␊
            <p className={"jsx-1800172487"}>dynamic element</p>␊
            <_JSXStyle id={"1800172487"}>{".root.jsx-1800172487{background:red;}"}</_JSXStyle>␊
          </Element>;␊
      }␊
    }␊
    ␊
    const Element2 = 'div';␊
    export const Test2 = class {␊
      render() {␊
        return <Element2 className="root">␊
            <p className={"jsx-1800172487"}>dynamic element</p>␊
            <_JSXStyle id={"1800172487"}>{".root.jsx-1800172487{background:red;}"}</_JSXStyle>␊
          </Element2>;␊
      }␊
    };`

## works with expressions in template literals

> Snapshot 1

    `import _JSXStyle from 'styled-jsx/style';␊
    const darken = c => c;␊
    const color = 'red';␊
    const otherColor = 'green';␊
    const mediumScreen = '680px';␊
    const animationDuration = '200ms';␊
    const animationName = 'my-cool-animation';␊
    const obj = { display: 'block' };␊
    ␊
    export default (({ display }) => <div className={'jsx-3956171631 ' + _JSXStyle.dynamic([['2143443147', [darken(color)]], ['2381675492', [darken(color) + 2]], ['3830663176', [display ? 'block' : 'none']], ['1555166447', [display ? 'block' : 'none']]])}>␊
        <p className={'jsx-3956171631 ' + _JSXStyle.dynamic([['2143443147', [darken(color)]], ['2381675492', [darken(color) + 2]], ['3830663176', [display ? 'block' : 'none']], ['1555166447', [display ? 'block' : 'none']]])}>test</p>␊
        <_JSXStyle id={"1003380713"}>{`p.${color}.jsx-3956171631{color:${otherColor};display:${obj.display};}`}</_JSXStyle>␊
        <_JSXStyle id={"2743241663"}>{"p.jsx-3956171631{color:red;}"}</_JSXStyle>␊
        <_JSXStyle id={"602592955"}>{`body{background:${color};}`}</_JSXStyle>␊
        <_JSXStyle id={"602592955"}>{`body{background:${color};}`}</_JSXStyle>␊
        <_JSXStyle id={"128557999"}>{`p.jsx-3956171631{color:${color};}`}</_JSXStyle>␊
        <_JSXStyle id={"128557999"}>{`p.jsx-3956171631{color:${color};}`}</_JSXStyle>␊
        <_JSXStyle id={"2143443147"} dynamic={[darken(color)]}>{`p.__jsx-style-dynamic-selector{color:${darken(color)};}`}</_JSXStyle>␊
        <_JSXStyle id={"2381675492"} dynamic={[darken(color) + 2]}>{`p.__jsx-style-dynamic-selector{color:${darken(color) + 2};}`}</_JSXStyle>␊
        <_JSXStyle id={"309852217"}>{`@media (min-width:${mediumScreen}){p.jsx-3956171631{color:green;}p.jsx-3956171631{color:${`red`};}}p.jsx-3956171631{color:red;}`}</_JSXStyle>␊
        <_JSXStyle id={"2824547816"}>{`p.jsx-3956171631{-webkit-animation-duration:${animationDuration};animation-duration:${animationDuration};}`}</_JSXStyle>␊
        <_JSXStyle id={"417951176"}>{`p.jsx-3956171631{-webkit-animation:${animationDuration} forwards ${animationName};animation:${animationDuration} forwards ${animationName};}div.jsx-3956171631{background:${color};}`}</_JSXStyle>␊
    ␊
        <_JSXStyle id={"3830663176"} dynamic={[display ? 'block' : 'none']}>{`span.__jsx-style-dynamic-selector{display:${display ? 'block' : 'none'};}`}</_JSXStyle>␊
        <_JSXStyle id={"1555166447"} dynamic={[display ? 'block' : 'none']}>{`span.__jsx-style-dynamic-selector:before{display:${display ? 'block' : 'none'};content:'\\`';}`}</_JSXStyle>␊
      </div>);`

## works with global styles

> Snapshot 1

    `import _JSXStyle from 'styled-jsx/style';␊
    const Test = () => <div className={"jsx-2209073070"}>␊
        <_JSXStyle id={"2209073070"}>{"body{color:red;}:hover{color:red;display:-webkit-box;display:-webkit-flex;display:-ms-flexbox;display:flex;-webkit-animation:foo 1s ease-out;animation:foo 1s ease-out;}div a{display:none;}[data-test]>div{color:red;}"}</_JSXStyle>␊
      </div>;␊
    ␊
    const Test2 = () => <_JSXStyle id={"2743241663"}>{"p{color:red;}"}</_JSXStyle>;`

## works with multiple jsx blocks

> Snapshot 1

    `import _JSXStyle from "styled-jsx/style";␊
    const attrs = {␊
      id: 'test'␊
    };␊
    ␊
    const Test1 = () => <div className={"jsx-2529315885"}>␊
        <span {...attrs} data-test="test" className={"jsx-2529315885" + " " + (attrs && attrs.className != null && attrs.className || "")}>test</span>␊
        <Component />␊
        <_JSXStyle id={"2529315885"}>{"span.jsx-2529315885{color:red;}"}</_JSXStyle>␊
      </div>;␊
    ␊
    const Test2 = () => <span>test</span>;␊
    ␊
    const Test3 = () => <div className={"jsx-2529315885"}>␊
        <span className={"jsx-2529315885"}>test</span>␊
        <_JSXStyle id={"2529315885"}>{"span.jsx-2529315885{color:red;}"}</_JSXStyle>␊
      </div>;␊
    ␊
    export default class {␊
      render() {␊
        return <div className={"jsx-2101845350"}>␊
            <p className={"jsx-2101845350"}>test</p>␊
            <_JSXStyle id={"2101845350"}>{"p.jsx-2101845350{color:red;}"}</_JSXStyle>␊
          </div>;␊
      }␊
    }`

## works with non styled-jsx styles

> Snapshot 1

    `import _JSXStyle from 'styled-jsx/style';␊
    export default (() => <div className={"jsx-2743241663"}>␊
        <p className={"jsx-2743241663"}>woot</p>␊
        <style dangerouslySetInnerHTML={{ __html: `body { margin: 0; }` }}></style>␊
        <_JSXStyle id={"2743241663"}>{"p.jsx-2743241663{color:red;}"}</_JSXStyle>␊
      </div>);`

## works with stateless

> Snapshot 1

    `import _JSXStyle from 'styled-jsx/style';␊
    export default (() => <div className={"jsx-2743241663"}>␊
        <p className={"jsx-2743241663"}>test</p>␊
        <p className={"jsx-2743241663"}>woot</p>␊
        <p className={"jsx-2743241663"}>woot</p>␊
        <_JSXStyle id={"2743241663"}>{"p.jsx-2743241663{color:red;}"}</_JSXStyle>␊
      </div>);`