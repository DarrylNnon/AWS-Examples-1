
## Create our bucket
```sh
aws s3 mb s3://prefixes-fun-fd
```

## Create our folder

```sh
aws s3api put-object --bucket="prefixes-fun-fd" --key="hello/"
```

## Create many folders
```sh
aws s3api put-object --bucket="prefixes-fun-fd" --key="Lorem/ipsum/dolor/sit/amet/consectetur/adipiscing/elit/Pellentesque/eu/quam/lacus/Orci/varius/natoque/penatibus/et/magnis/dis/parturient/montes/nascetur/ridiculus/mus/Cras/sollicitudin/massa/sed/elit/luctus/eget/fringilla/purus/fringilla/Ut/non/ornare/dui/Et/iam/eu/ex/id/ex/dictum/eleifend/Nunc/vitae/commodo/neque/eu/scelerisque/tellus/Nulla/facilisi/Curabitur/sed/neque/malesuada/consequat/lorem/ac/tincidunt/urna/Morbi/ac/enim/tellus/Curabitur/vel/erat/Duis/luctus/id/turpis/a/placerat/Et/iam/egestas/elementum/quam/id/maximus/felis/dignissim/sed/Morbi/ut/facilisis/mauris/Pellentesque/lacus/faucibus/finibus/eu/elit/Ut/dapibus/enim/lacus/nec/consequat/quam/consectetur/ac/Ut/vulputate/molestie/velit/eget/pretium/justo/sodales/vitae/Nunc/id/sollicitudin/tellus/Suspendisse/potenti/Aliquam/rutrum/odio/molestie/pulvinar/ipsum/mi/ullamcorper/non/sollicitudin/ligula/orci/ex/Cras/pharetra/feugiat/rutrum/In/interdum/pellentesque/turpis/love/money/lover/beauty/life/argent/beaute/happy/keaj/list/bonne/chanceux/lo/mama/pomme/fruite/beau/loveee/"
```

### Try and break the 1024 limit

```sh
aws s3api put-object --bucket="prefixes-fun-fd" --key="Lorem/ipsum/dolor/sit/amet/consectetur/adipiscing/elit/Nunc/id/facilisis/dolor/Donec/laoreet/odio/ac/bibendum/eleifend/Ut/nunc/massa/finibus/vitae/hendrerit/ac/aliquam/in/ligula/Vestibulum/eu/nibh/eget/nisl/aliquet/elementum/id/non/massa/Praesent/sed/dolor/facilisis/imperdiet/justo/ut/varius/urna/Cras/lacinia/lacinia/diam/sed/convallis/nisi/vehicula/sit/amet/Mauris/lacinia/rutrum/justo/a/consectetur/dolor/maximus/et/Duis/condimentum/dignissim/ligula/et/sollicitudin/Mauris/non/convallis/nisi/eget/vestibulum/est/Aliquam/faucibus/vestibulum/lacus/vitae/sagittis/nulla/blandit/quis/Vivamus/vel/justo/a/nisi/bibendum/varius/ac/vitae/urna/Nullam/et/lorem/metus/Praesent/lorem/mi/laoreet/eget/tincidunt/et/vestibulum/eget/erat/Aenean/nisl/ante/lobortis/vel/orci/sit/amet/commodo/viverra/mauris/Fusce/at/ipsum/at/ex/facilisis/ultrices/et/vel/augue/Etiam/vitae/nulla/sit/amet/risus/sagittis/pharetra/ullamcorper/vitae/mi/Nullam/eget/mollis/urna/non/malesuada/dui/Morbi/porta/nunc/et/ipsum/libero/wra/dsf/dfs/gf/dhg/gfh/jgidngi/hello.txt" --body="hello.txt"
```