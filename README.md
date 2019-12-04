cf create-service xsuaa application HAA_UAA -c xs-security.json

mta --build-target=CF --mtar=target/cf_haa_CF.mtar build
cf deploy target/cf_haa_CF.mtar

mta --build-target=CF --mtar=target/cf_haa_CF.mtar build ; cf deploy target/cf_haa_CF.mtar

mta --build-target=CF --mtar=target/haa-isveng2.mtar build ; cf deploy target/haa-isveng2.mtar -e mta_to_cf-dev.mtaext
