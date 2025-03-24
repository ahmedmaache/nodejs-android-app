FROM node:20
RUN apt-get update && apt-get install -y openjdk-17-jdk
RUN wget https://dl.google.com/android/repository/commandlinetools-linux-10406996_latest.zip && \
    unzip commandlinetools-linux-10406996_latest.zip -d android-sdk && \
    rm commandlinetools-linux-10406996_latest.zip
ENV ANDROID_HOME=/workspace/android-sdk
ENV PATH=${PATH}:${ANDROID_HOME}/cmdline-tools/latest/bin
RUN yes | sdkmanager "platform-tools" "platforms;android-34"
RUN npm install -g androidjs-builder
