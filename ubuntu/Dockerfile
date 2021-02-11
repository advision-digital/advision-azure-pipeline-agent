FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y --no-install-recommends															\
	ca-certificates gpg	apt-transport-https																					\
	libc6 libgcc1 libgssapi-krb5-2 libicu66 libssl1.1 zlib1g 																\
	libstdc++6 liblttng-ust-ctl4 libnuma1 liburcu6 liblttng-ust0 															\
	git curl													  															&&\
	curl -s https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor -o /etc/apt/trusted.gpg.d/microsoft.asc.gpg	&&\
	curl -s https://packages.microsoft.com/config/ubuntu/20.04/prod.list -o /etc/apt/sources.list.d/microsoft-prod.list		&&\
	apt-get update && apt-get install -y --no-install-recommends dotnet-sdk-5.0 											&&\
	apt-get upgrade -y && apt-get autoremove && apt-get clean -y  															&&\
	rm -rf /var/lib/apt/lists/*

ENV DOTNET_CLI_TELEMETRY_OPTOUT = "1"
WORKDIR /azp
COPY ./start.sh .
RUN chmod +x start.sh
CMD ["./start.sh"]