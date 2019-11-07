cf create-service xsuaa application HAA_UAA -c xs-security.json

mta --build-target=CF --mtar=target/cf_haa_CF.mtar build
cf deploy target/cf_haa_CF.mtar
