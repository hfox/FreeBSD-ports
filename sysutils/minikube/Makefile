PORTNAME=	minikube
PORTVERSION=	1.28.0
PORTREVISION=	4
DISTVERSIONPREFIX=	v
CATEGORIES=	sysutils

MAINTAINER=	danilo@FreeBSD.org
COMMENT=	Run Kubernetes locally
WWW=		https://github.com/kubernetes/minikube

LICENSE=	APACHE20

BUILD_DEPENDS=	go-bindata:devel/go-bindata

USES=		cpe go:modules
CPE_VENDOR=	kubernetes

USE_GITHUB=	yes
GH_ACCOUNT=	kubernetes
GH_TUPLE=	\
		Azure:go-ansiterm:d185dfc1b5a1:azure_go_ansiterm/vendor/github.com/Azure/go-ansiterm \
		Delta456:box-cli-maker:v2.3.0:delta456_box_cli_maker_v2/vendor/github.com/Delta456/box-cli-maker/v2 \
		GoogleCloudPlatform:docker-credential-gcr:faed5e8b8ca2:googlecloudplatform_docker_credential_gcr/vendor/github.com/GoogleCloudPlatform/docker-credential-gcr \
		GoogleCloudPlatform:opentelemetry-operations-go:2bf913f63d72:googlecloudplatform_opentelemetry_operations_go_trace \
		GoogleCloudPlatform:opentelemetry-operations-go:v0.34.1:googlecloudplatform_opentelemetry_operations_go_resourcemapping/vendor/github.com/GoogleCloudPlatform/opentelemetry-operations-go \
		MakeNowJust:heredoc:v1.0.0:makenowjust_heredoc/vendor/github.com/MakeNowJust/heredoc \
		Microsoft:go-winio:v0.6.0:microsoft_go_winio/vendor/github.com/Microsoft/go-winio \
		Microsoft:hcsshim:v0.8.17:microsoft_hcsshim/vendor/github.com/Microsoft/hcsshim \
		Parallels:docker-machine-parallels:v2.0.1:parallels_docker_machine_parallels_v2/vendor/github.com/Parallels/docker-machine-parallels/v2 \
		PuerkitoBio:purell:v1.1.1:puerkitobio_purell/vendor/github.com/PuerkitoBio/purell \
		PuerkitoBio:urlesc:de5bf2ad4578:puerkitobio_urlesc/vendor/github.com/PuerkitoBio/urlesc \
		VividCortex:ewma:v1.1.1:vividcortex_ewma/vendor/github.com/VividCortex/ewma \
		VividCortex:godaemon:v1.0.0:vividcortex_godaemon/vendor/github.com/VividCortex/godaemon \
		Xuanwo:go-locale:v1.1.0:xuanwo_go_locale/vendor/github.com/Xuanwo/go-locale \
		ajstarks:svgo:1546f124cd8b:ajstarks_svgo/vendor/github.com/ajstarks/svgo \
		alonyb:spinner:v1.12.7:alonyb_spinner/vendor/github.com/briandowns/spinner \
		apache:thrift:2566ecd5d999:apache_thrift/vendor/git.apache.org/thrift.git \
		aws:aws-sdk-go:v1.38.49:aws_aws_sdk_go/vendor/github.com/aws/aws-sdk-go \
		beorn7:perks:v1.0.1:beorn7_perks/vendor/github.com/beorn7/perks \
		bgentry:go-netrc:9fd32a8b3d3d:bgentry_go_netrc/vendor/github.com/bgentry/go-netrc \
		blang:semver:v4.0.0:blang_semver/vendor/github.com/blang/semver \
		c4milo:gotoolkit:67483a18c17a:c4milo_gotoolkit/vendor/github.com/c4milo/gotoolkit \
		cenkalti:backoff:v4.1.3:cenkalti_backoff_v4/vendor/github.com/cenkalti/backoff/v4 \
		census-ecosystem:opencensus-go-exporter-stackdriver:v0.13.12:census_ecosystem_opencensus_go_exporter_stackdriver/vendor/contrib.go.opencensus.io/exporter/stackdriver \
		census-instrumentation:opencensus-go:v0.23.0:census_instrumentation_opencensus_go/vendor/go.opencensus.io \
		census-instrumentation:opencensus-proto:v0.3.0:census_instrumentation_opencensus_proto/vendor/github.com/census-instrumentation/opencensus-proto \
		cespare:xxhash:v2.1.2:cespare_xxhash_v2/vendor/github.com/cespare/xxhash/v2 \
		cheggaaa:pb:v3.1.0:cheggaaa_pb_v3/vendor/github.com/cheggaaa/pb \
		cloudevents:sdk-go:v2.12.0:cloudevents_sdk_go_v2/vendor/github.com/cloudevents/sdk-go \
		containerd:cgroups:v1.0.1:containerd_cgroups/vendor/github.com/containerd/cgroups \
		containerd:containerd:v1.5.2:containerd_containerd/vendor/github.com/containerd/containerd \
		containerd:stargz-snapshotter:v0.12.1:containerd_stargz_snapshotter_estargz/vendor/github.com/containerd/stargz-snapshotter \
		coreos:go-systemd:v22.3.2:coreos_go_systemd_v22/vendor/github.com/coreos/go-systemd/v22 \
		cpuguy83:go-md2man:v2.0.2:cpuguy83_go_md2man_v2/vendor/github.com/cpuguy83/go-md2man/v2 \
		cyphar:filepath-securejoin:v0.2.3:cyphar_filepath_securejoin/vendor/github.com/cyphar/filepath-securejoin \
		davecgh:go-spew:v1.1.1:davecgh_go_spew/vendor/github.com/davecgh/go-spew \
		docker:cli:v20.10.20:docker_cli/vendor/github.com/docker/cli \
		docker:distribution:v2.8.1:docker_distribution/vendor/github.com/docker/distribution \
		docker:go-connections:v0.4.0:docker_go_connections/vendor/github.com/docker/go-connections \
		docker:go-units:v0.5.0:docker_go_units/vendor/github.com/docker/go-units \
		elazarl:goproxy:a92cc753f88e:elazarl_goproxy/vendor/github.com/elazarl/goproxy \
		emicklei:go-restful:v3.8.0:emicklei_go_restful_v3/vendor/github.com/emicklei/go-restful/v3 \
		evanphx:json-patch:v4.12.0:evanphx_json_patch/vendor/github.com/evanphx/json-patch \
		fatih:color:v1.13.0:fatih_color/vendor/github.com/fatih/color \
		fsnotify:fsnotify:v1.5.4:fsnotify_fsnotify/vendor/github.com/fsnotify/fsnotify \
		go-fonts:liberation:v0.2.0:go_fonts_liberation/vendor/github.com/go-fonts/liberation \
		go-inf:inf:v0.9.1:go_inf_inf/vendor/gopkg.in/inf.v0 \
		go-ini:ini:v1.67.0:go_ini_ini/vendor/gopkg.in/ini.v1 \
		go-latex:latex:c0d11ff05a81:go_latex_latex/vendor/github.com/go-latex/latex \
		go-logr:logr:v1.2.3:go_logr_logr/vendor/github.com/go-logr/logr \
		go-logr:stdr:v1.2.2:go_logr_stdr/vendor/github.com/go-logr/stdr \
		go-mgo:mgo:a6b53ec6cb22:go_mgo_mgo/vendor/gopkg.in/mgo.v2 \
		go-ole:go-ole:v1.2.6:go_ole_go_ole/vendor/github.com/go-ole/go-ole \
		go-openapi:jsonpointer:v0.19.5:go_openapi_jsonpointer/vendor/github.com/go-openapi/jsonpointer \
		go-openapi:jsonreference:v0.19.5:go_openapi_jsonreference/vendor/github.com/go-openapi/jsonreference \
		go-openapi:swag:v0.19.14:go_openapi_swag/vendor/github.com/go-openapi/swag \
		go-pdf:fpdf:v0.6.0:go_pdf_fpdf/vendor/github.com/go-pdf/fpdf \
		go-yaml:yaml:v2.4.0:go_yaml_yaml/vendor/gopkg.in/yaml.v2 \
		go-yaml:yaml:v3.0.1:go_yaml_yaml_1/vendor/gopkg.in/yaml.v3 \
		godbus:dbus:v5.0.6:godbus_dbus_v5/vendor/github.com/godbus/dbus/v5 \
		gogo:protobuf:v1.3.2:gogo_protobuf/vendor/github.com/gogo/protobuf \
		golang-collections:collections:604e922904d3:golang_collections_collections/vendor/github.com/golang-collections/collections \
		golang:appengine:v1.6.7:golang_appengine/vendor/google.golang.org/appengine \
		golang:build:2835ba2e683f:golang_build/vendor/golang.org/x/build \
		golang:crypto:v0.1.0:golang_crypto/vendor/golang.org/x/crypto \
		golang:exp:5c715a9e8561:golang_exp/vendor/golang.org/x/exp \
		golang:freetype:e2365dfdc4a0:golang_freetype/vendor/github.com/golang/freetype \
		golang:groupcache:41bb18bfe9da:golang_groupcache/vendor/github.com/golang/groupcache \
		golang:image:e7cb96979f69:golang_image/vendor/golang.org/x/image \
		golang:mod:v0.6.0:golang_mod/vendor/golang.org/x/mod \
		golang:net:v0.1.0:golang_net/vendor/golang.org/x/net \
		golang:oauth2:v0.1.0:golang_oauth2/vendor/golang.org/x/oauth2 \
		golang:protobuf:v1.5.2:golang_protobuf/vendor/github.com/golang/protobuf \
		golang:sync:v0.1.0:golang_sync/vendor/golang.org/x/sync \
		golang:sys:v0.1.0:golang_sys/vendor/golang.org/x/sys \
		golang:term:v0.1.0:golang_term/vendor/golang.org/x/term \
		golang:text:v0.4.0:golang_text/vendor/golang.org/x/text \
		golang:time:90d013bbcef8:golang_time/vendor/golang.org/x/time \
		golang:tools:v0.1.12:golang_tools/vendor/golang.org/x/tools \
		golang:xerrors:04be3eba64a2:golang_xerrors/vendor/golang.org/x/xerrors \
		google:gnostic:v0.5.7-v3refs:google_gnostic/vendor/github.com/google/gnostic \
		google:go-cmp:v0.5.9:google_go_cmp/vendor/github.com/google/go-cmp \
		google:go-containerregistry:v0.12.0:google_go_containerregistry/vendor/github.com/google/go-containerregistry \
		google:go-genproto:99cd37c6964a:google_go_genproto/vendor/google.golang.org/genproto \
		google:go-github:v43.0.0:google_go_github_v43/vendor/github.com/google/go-github/v43 \
		google:go-querystring:v1.1.0:google_go_querystring/vendor/github.com/google/go-querystring \
		google:gofuzz:v1.1.0:google_gofuzz/vendor/github.com/google/gofuzz \
		google:slowjam:v1.0.0:google_slowjam/vendor/github.com/google/slowjam \
		google:uuid:v1.3.0:google_uuid/vendor/github.com/google/uuid \
		googleapis:enterprise-certificate-proxy:v0.2.0:googleapis_enterprise_certificate_proxy/vendor/github.com/googleapis/enterprise-certificate-proxy \
		googleapis:gax-go:v2.6.0:googleapis_gax_go_v2/vendor/github.com/googleapis/gax-go \
		googleapis:google-api-go-client:v0.100.0:googleapis_google_api_go_client/vendor/google.golang.org/api \
		googleapis:google-cloud-go:compute/v1.10.0:googleapis_google_cloud_go_compute \
		googleapis:google-cloud-go:monitoring/v1.1.0:googleapis_google_cloud_go_monitoring \
		googleapis:google-cloud-go:storage/v1.27.0:googleapis_google_cloud_go_storage \
		googleapis:google-cloud-go:trace/v1.2.0:googleapis_google_cloud_go_trace \
		googleapis:google-cloud-go:v0.104.0:googleapis_google_cloud_go_iam/vendor/cloud.google.com/go \
		gookit:color:v1.5.2:gookit_color/vendor/github.com/gookit/color \
		grpc:grpc-go:v1.50.1:grpc_grpc_go/vendor/google.golang.org/grpc \
		hashicorp:go-cleanhttp:v0.5.2:hashicorp_go_cleanhttp/vendor/github.com/hashicorp/go-cleanhttp \
		hashicorp:go-getter:v1.6.2:hashicorp_go_getter/vendor/github.com/hashicorp/go-getter \
		hashicorp:go-retryablehttp:v0.7.1:hashicorp_go_retryablehttp/vendor/github.com/hashicorp/go-retryablehttp \
		hashicorp:go-safetemp:v1.0.0:hashicorp_go_safetemp/vendor/github.com/hashicorp/go-safetemp \
		hashicorp:go-version:v1.2.1:hashicorp_go_version/vendor/github.com/hashicorp/go-version \
		hashicorp:hcl:v1.0.0:hashicorp_hcl/vendor/github.com/hashicorp/hcl \
		hectane:go-acl:da78bae5fc95:hectane_go_acl/vendor/github.com/hectane/go-acl \
		hooklift:assert:9d1defd6d214:hooklift_assert/vendor/github.com/hooklift/assert \
		hooklift:iso9660:1cf07e5970d8:hooklift_iso9660/vendor/github.com/hooklift/iso9660 \
		huandu:xstrings:v1.3.2:huandu_xstrings/vendor/github.com/huandu/xstrings \
		imdario:mergo:v0.3.11:imdario_mergo/vendor/github.com/imdario/mergo \
		inconshreveable:mousetrap:v1.0.1:inconshreveable_mousetrap/vendor/github.com/inconshreveable/mousetrap \
		intel-go:cpuid:1a4a6f06a1c6:intel_go_cpuid/vendor/github.com/intel-go/cpuid \
		jmespath:go-jmespath:v0.4.0:jmespath_go_jmespath/vendor/github.com/jmespath/go-jmespath \
		johanneswuerbach:nfsexports:c48c3734757f:johanneswuerbach_nfsexports/vendor/github.com/johanneswuerbach/nfsexports \
		josharian:intern:v1.0.0:josharian_intern/vendor/github.com/josharian/intern \
		json-iterator:go:v1.1.12:json_iterator_go/vendor/github.com/json-iterator/go \
		juju:clock:9c5c9712527c:juju_clock/vendor/github.com/juju/clock \
		juju:errors:0232dcc7464d:juju_errors/vendor/github.com/juju/errors \
		juju:fslock:4d5c94c67b4b:juju_fslock/vendor/github.com/juju/fslock \
		juju:loggo:6e530bcce5d8:juju_loggo/vendor/github.com/juju/loggo \
		juju:mutex:d21b13acf4bf:juju_mutex/vendor/github.com/juju/mutex \
		juju:retry:9058e192b216:juju_retry/vendor/github.com/juju/retry \
		juju:testing:ce30eb24acd2:juju_testing/vendor/github.com/juju/testing \
		juju:utils:bf9cc5bdd62d:juju_utils/vendor/github.com/juju/utils \
		juju:version:b64dbd566305:juju_version/vendor/github.com/juju/version \
		kballard:go-shellquote:95032a82bc51:kballard_go_shellquote/vendor/github.com/kballard/go-shellquote \
		klauspost:compress:v1.15.11:klauspost_compress/vendor/github.com/klauspost/compress \
		klauspost:cpuid:v1.2.0:klauspost_cpuid/vendor/github.com/klauspost/cpuid \
		kubernetes-sigs:json:f223a00ba0e2:kubernetes_sigs_json/vendor/sigs.k8s.io/json \
		kubernetes-sigs:sig-storage-lib-external-provisioner:v6.3.0:kubernetes_sigs_sig_storage_lib_external_provisioner/vendor/sigs.k8s.io/sig-storage-lib-external-provisioner/v6 \
		kubernetes-sigs:structured-merge-diff:v4.2.3:kubernetes_sigs_structured_merge_diff/vendor/sigs.k8s.io/structured-merge-diff/v4 \
		kubernetes-sigs:yaml:v1.2.0:kubernetes_sigs_yaml/vendor/sigs.k8s.io/yaml \
		kubernetes:api:v0.25.3:kubernetes_api/vendor/k8s.io/api \
		kubernetes:apimachinery:v0.25.3:kubernetes_apimachinery/vendor/k8s.io/apimachinery \
		kubernetes:client-go:v0.25.3:kubernetes_client_go/vendor/k8s.io/client-go \
		kubernetes:cluster-bootstrap:v0.22.4:kubernetes_cluster_bootstrap/vendor/k8s.io/cluster-bootstrap \
		kubernetes:component-base:v0.25.3:kubernetes_component_base/vendor/k8s.io/component-base \
		kubernetes:klog:v2.80.1:kubernetes_klog/vendor/k8s.io/klog/v2 \
		kubernetes:kube-openapi:67bda5d908f1:kubernetes_kube_openapi/vendor/k8s.io/kube-openapi \
		kubernetes:kubectl:v0.25.3:kubernetes_kubectl/vendor/k8s.io/kubectl \
		kubernetes:utils:ee6ede2d64ed:kubernetes_utils/vendor/k8s.io/utils \
		lufia:plan9stats:39d0f177ccd0:lufia_plan9stats/vendor/github.com/lufia/plan9stats \
		machine-drivers:docker-machine-driver-vmware:v0.1.5:machine_drivers_docker_machine_driver_vmware/vendor/github.com/machine-drivers/docker-machine-driver-vmware \
		machine-drivers:machine:78a84df85426:machine_drivers_machine/vendor/github.com/docker/machine \
		magiconair:properties:v1.8.6:magiconair_properties/vendor/github.com/magiconair/properties \
		mailru:easyjson:v0.7.6:mailru_easyjson/vendor/github.com/mailru/easyjson \
		mattbaird:jsonpatch:098863c1fc24:mattbaird_jsonpatch/vendor/github.com/mattbaird/jsonpatch \
		mattn:go-colorable:v0.1.12:mattn_go_colorable/vendor/github.com/mattn/go-colorable \
		mattn:go-isatty:v0.0.16:mattn_go_isatty/vendor/github.com/mattn/go-isatty \
		mattn:go-runewidth:v0.0.14:mattn_go_runewidth/vendor/github.com/mattn/go-runewidth \
		matttproud:golang_protobuf_extensions:c182affec369:matttproud_golang_protobuf_extensions/vendor/github.com/matttproud/golang_protobuf_extensions \
		miekg:dns:v1.1.41:miekg_dns/vendor/github.com/miekg/dns \
		mitchellh:go-homedir:v1.1.0:mitchellh_go_homedir/vendor/github.com/mitchellh/go-homedir \
		mitchellh:go-ps:v1.0.0:mitchellh_go_ps/vendor/github.com/mitchellh/go-ps \
		mitchellh:go-testing-interface:v1.0.0:mitchellh_go_testing_interface/vendor/github.com/mitchellh/go-testing-interface \
		mitchellh:go-wordwrap:v1.0.0:mitchellh_go_wordwrap/vendor/github.com/mitchellh/go-wordwrap \
		mitchellh:mapstructure:v1.5.0:mitchellh_mapstructure/vendor/github.com/mitchellh/mapstructure \
		moby:hyperkit:2f061e447e14:moby_hyperkit/vendor/github.com/moby/hyperkit \
		docker:docker-credential-helpers:v0.7.0:docker_docker_credential_helpers/vendor/github.com/docker/docker-credential-helpers \
		moby:moby:v20.10.21:moby_moby/vendor/github.com/docker/docker \
		moby:spdystream:v0.2.0:moby_spdystream/vendor/github.com/moby/spdystream \
		moby:sys:mount/v0.2.0:moby_sys_mount/vendor/github.com/moby/sys \
		moby:sys:mountinfo/v0.5.0:moby_sys_mountinfo \
		moby:term:3f7ff695adc6:moby_term/vendor/github.com/moby/term \
		modern-go:concurrent:bacd9c7ef1dd:modern_go_concurrent/vendor/github.com/modern-go/concurrent \
		modern-go:reflect2:v1.0.2:modern_go_reflect2/vendor/github.com/modern-go/reflect2 \
		muesli:reflow:v0.3.0:muesli_reflow/vendor/github.com/muesli/reflow \
		munnerz:goautoneg:a7dc8b61c822:munnerz_goautoneg/vendor/github.com/munnerz/goautoneg \
		olekukonko:tablewriter:v0.0.5:olekukonko_tablewriter/vendor/github.com/olekukonko/tablewriter \
		open-telemetry:opentelemetry-go:v1.11.1:open_telemetry_opentelemetry_go/vendor/go.opentelemetry.io/otel \
		opencontainers:go-digest:v1.0.0:opencontainers_go_digest/vendor/github.com/opencontainers/go-digest \
		opencontainers:image-spec:v1.1.0-rc2:opencontainers_image_spec/vendor/github.com/opencontainers/image-spec \
		opencontainers:runc:v1.1.4:opencontainers_runc/vendor/github.com/opencontainers/runc \
		opencontainers:runtime-spec:1c3f411f0417:opencontainers_runtime_spec/vendor/github.com/opencontainers/runtime-spec \
		otiai10:copy:v1.7.0:otiai10_copy/vendor/github.com/otiai10/copy \
		pborman:uuid:v1.2.1:pborman_uuid/vendor/github.com/pborman/uuid \
		pelletier:go-toml:v1.9.5:pelletier_go_toml/vendor/github.com/pelletier/go-toml \
		pelletier:go-toml:v2.0.5:pelletier_go_toml_v2/vendor/github.com/pelletier/go-toml/v2 \
		phayes:freeport:95f893ade6f2:phayes_freeport/vendor/github.com/phayes/freeport \
		pkg:browser:9302be274faa:pkg_browser/vendor/github.com/pkg/browser \
		pkg:errors:v0.9.1:pkg_errors/vendor/github.com/pkg/errors \
		pkg:profile:3a8809bd8a80:pkg_profile/vendor/github.com/pkg/profile \
		pmezard:go-difflib:v1.0.0:pmezard_go_difflib/vendor/github.com/pmezard/go-difflib \
		power-devops:perfstat:5aafc221ea8c:power_devops_perfstat/vendor/github.com/power-devops/perfstat \
		prometheus:client_golang:v1.12.1:prometheus_client_golang/vendor/github.com/prometheus/client_golang \
		prometheus:client_model:v0.2.0:prometheus_client_model/vendor/github.com/prometheus/client_model \
		prometheus:common:v0.32.1:prometheus_common/vendor/github.com/prometheus/common \
		prometheus:procfs:v0.7.3:prometheus_procfs/vendor/github.com/prometheus/procfs \
		prometheus:prometheus:v2.5.0:prometheus_prometheus/vendor/github.com/prometheus/prometheus \
		protocolbuffers:protobuf-go:v1.28.1:protocolbuffers_protobuf_go/vendor/google.golang.org/protobuf \
		rivo:uniseg:v0.2.0:rivo_uniseg/vendor/github.com/rivo/uniseg \
		russross:blackfriday:v1.6.0:russross_blackfriday/vendor/github.com/russross/blackfriday \
		russross:blackfriday:v2.1.0:russross_blackfriday_v2/vendor/github.com/russross/blackfriday/v2 \
		santhosh-tekuri:jsonschema:v5.0.2:santhosh_tekuri_jsonschema_v5/vendor/github.com/santhosh-tekuri/jsonschema/v5 \
		sayboras:dockerclient:v1.0.0:sayboras_dockerclient/vendor/github.com/samalba/dockerclient \
		shirou:gopsutil:v3.22.9:shirou_gopsutil_v3/vendor/github.com/shirou/gopsutil/v3 \
		sirupsen:logrus:v1.9.0:sirupsen_logrus/vendor/github.com/sirupsen/logrus \
		spf13:afero:v1.8.2:spf13_afero/vendor/github.com/spf13/afero \
		spf13:cast:v1.5.0:spf13_cast/vendor/github.com/spf13/cast \
		spf13:cobra:v1.6.1:spf13_cobra/vendor/github.com/spf13/cobra \
		spf13:jwalterweatherman:v1.1.0:spf13_jwalterweatherman/vendor/github.com/spf13/jwalterweatherman \
		spf13:pflag:v1.0.5:spf13_pflag/vendor/github.com/spf13/pflag \
		spf13:viper:v1.13.0:spf13_viper/vendor/github.com/spf13/viper \
		subosito:gotenv:v1.4.1:subosito_gotenv/vendor/github.com/subosito/gotenv \
		tklauser:go-sysconf:v0.3.10:tklauser_go_sysconf/vendor/github.com/tklauser/go-sysconf \
		tklauser:numcpus:v0.4.0:tklauser_numcpus/vendor/github.com/tklauser/numcpus \
		uber-go:atomic:v1.7.0:uber_go_atomic/vendor/go.uber.org/atomic \
		uber-go:multierr:v1.8.0:uber_go_multierr/vendor/go.uber.org/multierr \
		uber-go:zap:v1.19.0:uber_go_zap/vendor/go.uber.org/zap \
		ulikunitz:xz:v0.5.8:ulikunitz_xz/vendor/github.com/ulikunitz/xz \
		vbatts:tar-split:v0.11.2:vbatts_tar_split/vendor/github.com/vbatts/tar-split \
		xo:terminfo:abceb7e1c41e:xo_terminfo/vendor/github.com/xo/terminfo \
		yusufpapurcu:wmi:v1.2.2:yusufpapurcu_wmi/vendor/github.com/yusufpapurcu/wmi \
		zchee:go-vmnet:97ebf9174097:zchee_go_vmnet/vendor/github.com/zchee/go-vmnet

GL_TUPLE=	libvirt:libvirt-go-module:268a5d02e00cc9b3d5d7fa6c08d753071e7d14b8:libvirt_libvirt_go_module/vendor/libvirt.org/go/libvirt

GO_TARGET=	./cmd/${PORTNAME}
GO_BUILDFLAGS=	-ldflags="-X k8s.io/minikube/pkg/version.version=v${PORTVERSION} \
		-X k8s.io/minikube/pkg/version.isoVersion=v1.28.0 \
		-X k8s.io/minikube/pkg/version.storageProvisionerVersion=v5 \
		-X k8s.io/minikube/pkg/version.isoPath=minikube/iso"

PLIST_FILES=	bin/${PORTNAME}

SUB_FILES=	pkg-message

post-extract:
	@${RM} -r ${WRKSRC}/vendor/github.com/GoogleCloudPlatform/opentelemetry-operations-go/exporter/trace
	@${RLN} ${WRKSRC_googlecloudplatform_opentelemetry_operations_go_trace}/exporter/trace ${WRKSRC}/vendor/github.com/GoogleCloudPlatform/opentelemetry-operations-go/exporter/trace
	@${RM} -r ${WRKSRC}/vendor/github.com/moby/sys/mountinfo
	@${RLN} ${WRKSRC_moby_sys_mountinfo}/mountinfo ${WRKSRC}/vendor/github.com/moby/sys/mountinfo

post-patch:
	cd ${WRKSRC}/vendor/github.com/pkg/browser && \
		${LN} -s browser_linux.go browser_freebsd.go

pre-build:
	cd ${WRKSRC} && \
		${LOCALBASE}/bin/go-bindata -nomemcopy \
		-o pkg/minikube/assets/assets.go -pkg assets deploy/addons/... && \
		${LOCALBASE}/bin/go-bindata -nomemcopy \
		-o pkg/minikube/translate/translations.go -pkg translate translations/... && \
		${LOCALBASE}/bin/gofmt${GO_SUFFIX} -s -w pkg/minikube/translate/translations.go

.include <bsd.port.mk>
