FROM ubuntu:20.04

ENV USERNAME=vstsagent
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y --no-install-recommends		\
        ca-certificates 												\
		libc6 libgcc1 libgssapi-krb5-2 libicu66 libssl1.1 zlib1g 		\
		libstdc++6 liblttng-ust-ctl4 libnuma1 liburcu6 liblttng-ust0 	\
		git curl													  &&\
		apt-get upgrade -y && apt-get clean && apt-get autoremove -y  &&\
		rm -rf /var/lib/apt/lists/*

WORKDIR /azp
COPY ./start.sh .
RUN chmod +x start.sh
CMD ["./start.sh"]