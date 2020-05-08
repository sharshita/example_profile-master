# example_profile-master
#need to remove all UUIDs (Universally Unique Identifier) and default_config_hash to avoid conflicts. It can be easily executed #using command lines as mentioned below.
#for windows:

find /path/to/PROFILE_NAME/config/install/ -type f -exec sed -i -e '/^uuid: /d' {} \;
find /path/to/PROFILE_NAME/config/install/ -type f -exec sed -i -e '/_core/,+1d' {} \;

For mac osx:

find /path/to/PROFILE_NAME/config/install/ -type f -exec sed -i '' '/^uuid: /d' {} \;
find /path/to/PROFILE_NAME/config/install/ -type f -exec sed -i '' '/_core/{N;d;}' {} \;
