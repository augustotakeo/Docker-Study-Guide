FROM ubuntu:latest
ARG ARG_PASSED1
ARG ARG_PASSED2
ARG ARG_DEFAULT=defaultValue
ENV ENV_PASSED1=${ARG_PASSED1:-env_passed1_default}
ENV ENV_PASSED2=${ARG_PASSED2:-env_passed2_default}
ENV ENV_DEFAULT=envDefault
WORKDIR /app
RUN echo ${ARG_PASSED1} > arq_passed1.txt
RUN echo ${ARG_PASSED2} > arq_passed2.txt
RUN echo ${ARG_DEFAULT} > arq_default.txt
