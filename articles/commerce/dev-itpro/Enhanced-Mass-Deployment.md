---
title: Hromadné nasazení zapečetěných samoobslužných komponent Commerce
description: Tento článek vysvětluje, jak používat rámec pro samoobslužné instalační programy komponent k tiché instalaci a servisu nasazení.
author: jashanno
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 426473c14cdf9e171810aafd97dbb1afd5988b2f
ms.sourcegitcommit: 24673493d14f2045a08fe7240689bee34e099cb5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2022
ms.locfileid: "9589082"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Hromadné nasazení zapečetěných samoobslužných komponent Commerce

[!include [banner](../includes/banner.md)]

Tento článek se týká uzavřeného rámce, instalačních programů komponent, které jsou vydávány každý měsíc, počínaje verzí 10.0.18 a které jsou dostupné v knihovně sdílených aktiv v Microsoft Dynamics Lifecycle Services (LCS). Všimněte si, že prvních několik vydání těchto nových instalačních programů je označeno jako **(Preview)**. Jediným účelem tohoto označení je však odlišit nové instalační programy, zatímco společnost Microsoft určí, zda existují nějaké další funkční požadavky na jejich použití. Neznamená to, že instalační programy nejsou platné pro výrobu. Na základě vydání těchto nových instalačních programů Microsoft plánuje ukončit podporu starých (starších) instalačních programů v říjnu 2023 nebo kolem něj. 

Tento článek vysvětluje, jak používat nové instalační programy k provádění tiché instalace a servisu aktualizací pomocí argumentů příkazového řádku. Tyto argumenty umožňují hromadné nasazení několika různými způsoby.

> [!NOTE]
> Nové samoobslužné, zapečetěné instalační programy nebudou k dispozici v ústředí a lze je stáhnout pouze prostřednictvím LCS.

## <a name="delimiters-for-mass-deployment"></a>Oddělovače pro hromadné nasazení

Následující tabulka ukazuje oddělovače, které lze použít při provádění příkazového řádku.


| Oddělovač                 | Popis |
|---------------------------|-------------|
| -AadTokenIssuerPrefix | Předpona pro vydavatele tokenu Microsoft Azure Active Directory (Azure AD). |
| -AsyncClientAadClientId | ID klienta Azure AD, které by měl asynchronní klient používat při komunikaci s centrálou. |
| -AsyncClientAppInsightsInstrumentationKey | Klíč instrumentace AppInsights pro asynchronního klienta. |
| -AsyncClientCertFullPath | Plně formátovaná cesta URN, která používá kryptografický otisk jako vyhledávací metriku umístění certifikátu Async Client Identity, který má být použit k ověření v Azure AD pro komunikaci s centrálou. Například `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` je správně naformátovaná cesta URN. Hodnota **\<MyThumbprint\>** bude nahrazena kryptografickým otiskem certifikátu, který má být použit. Nepoužívejte tento parametr společně s parametrem **-AsyncClientCertThumbprint**. |
| -AsyncClientCertThumbprint | Kryptografický otisk certifikátu Async Client Identity, který má být použit k ověření Azure AD pro komunikaci s centrálou. Tento kryptografický otisk bude použit k vyhledání umístění **LocalMachine/My store** a názvu, abyste našli správný certifikát k použití. Nepoužívejte tento parametr společně s parametrem **-AsyncClientCertFullPath**. |
| -ClientAppInsightsInstrumentationKey | Klíč instrumentace AppInsights pro klienta. |
| -CloudPosAppInsightsInstrumentationKey | Klíč instrumentace AppInsights pro Cloud POS. |
| -Config | Konfigurační soubor, který by měl být použit během instalace. Příkladem názvu souboru je **Contoso.CommerceScaleUnit.xml**. |
| -CposAadClientId | ID klienta Azure AD, kterého má Cloud POS používat během aktivace zařízení. Tento parametr není vyžadován u místního nasazení. |
| -Device | ID zařízení, jak je uvedeno na stránce **Zařízení** v centrále. |
| -EnvironmentId | ID prostředí. |
| -HardwareStationAppInsightsInstrumentationKey | Klíč instrumentace hardwarové stanice AppInsights. |
| Nainstalovat | Parametr, který určuje, zda se má nainstalovat komponenta, kterou tento instalační program poskytuje. Tento parametr je vyžadován k provedení instalace a nemá úvodní pomlčku. |
| -InstallOffline | U Modern POS tento parametr určuje, že by měla být nainstalována a konfigurována také offline databáze. Použijte také parametr **-SQLServerName**. V opačném případě se instalační program pokusí najít výchozí instanci, která splňuje požadavky. Při použití ověřování Azure Active Directory (Azure AD) nebude POS offline fungovat, protože je vždy vyžadováno online připojení. |
| -Port | Port, který by měl být přidružen a používán virtuálním adresářem Retail Serveru. Pokud není nastaven žádný port, použije se výchozí port 443. |
| -Register | ID pokladny, jak je uvedeno na stránce **Pokladny** v centrále. |
| -RetailServerAadClientId | ID klienta Azure AD, které by měl Retail Server používat při komunikaci s centrálou. |
| -RetailServerAadResourceId | ID prostředku aplikace Azure AD Retail Serveru, který by měl být použit během aktivace zařízení. Tento parametr není vyžadován u místního nasazení. |
| -RetailServerCertFullPath | Plně formátovaná cesta URN, která používá kryptografický otisk jako vyhledávací metriku certifikátu Retail Server Identity, který má být použit k ověření v Azure AD pro komunikaci s centrálou. Například `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` je správně naformátovaná cesta URN, kde hodnota **\<MyThumbprint\>** bude nahrazena kryptografickým otiskem certifikátu, který má být použit. Nepoužívejte tento parametr společně s parametrem **-RetailServerCertThumbprint**. |
| -RetailServerCertThumbprint | Kryptografický otisk certifikátu Retail Server Identity, který má být použit k ověření Azure AD pro komunikaci s centrálou. Tento kryptografický otisk bude použit k vyhledání umístění obchodu **LocalMachine/My store** a názvu, abyste našli správný certifikát k použití. Nepoužívejte tento parametr společně s parametrem **-RetailServerCertFullPath**. |
| -RetailServerURL | Adresa URL Retail Serveru, který by měl instalační program použít. (Tato adresa URL je známá také jako adresa URL jednotky Commerce Scale Unit \[CSU\].) U Modern POS bude tato hodnota použita při aktivaci zařízení. |
| -SkipAadCredentialsCheck| Přepínač, který ukazuje, zda by měly být přeskočeny kontroly předpokladů pověření Azure AD. Výchozí hodnota je **false**. |
| -SkipCertCheck | Přepínač, který ukazuje, zda by měly být přeskočeny kontroly předpokladů certifikátu. Výchozí hodnota je **false**. |
| -SkipIisCheck | Přepínač, který ukazuje, zda by měly být přeskočeny kontroly předpokladů služeb IIS. Výchozí hodnota je **false**. |
| -SkipNetFrameworkCheck | Přepínač, který ukazuje, zda by měly být přeskočeny kontroly předpokladů prostředí .NET Framework. Výchozí hodnota je **false**. |
| -SkipScaleUnitHealthcheck | Přepínač, který označuje, zda má být přeskočena kontrola stavu nainstalovaných součástí. Výchozí hodnota je **false**. |
| -SkipSChannelCheck | Přepínač, který ukazuje, zda by měly být přeskočeny kontroly předpokladů zabezpečeného kanálu. Výchozí hodnota je **false**. |
| -SkipSqlFullTextCheck | Přepínač, který označuje, zda je třeba přeskočit ověření předpokladu serveru SQL Server, který vyžaduje fulltextové vyhledávání. Výchozí hodnota je **false**. |
| -SkipSqlServerCheck | Přepínač, který ukazuje, zda by měly být přeskočeny kontroly předpokladů SQL Serveru. Výchozí hodnota je **false**. |
| -SqlServerName | Název SQL Serveru. Pokud název nezadáte, instalační program se pokusí najít výchozí instanci. |
| -SslcertFullPath | Plně formátovaná cesta URN, která používá kryptografický otisk jako vyhledávací metriku umístění certifikátu, který má být použit k šifrování HTTP provozu do škálovací jednotky. Například `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` je správně naformátovaná cesta URN, kde hodnota **\<MyThumbprint\>** bude nahrazena kryptografickým otiskem certifikátu, který má být použit. Nepoužívejte tento parametr společně s parametrem **-SslCertThumbprint**. |
| -SslCertThumbprint | Kryptografický otisk certifikátu, který má být použit k šifrování provozu HTTP do škálovací jednotky. Tento kryptografický otisk bude použit k vyhledání umístění **LocalMachine/My store** a názvu, abyste našli správný certifikát k použití. Nepoužívejte tento parametr společně s parametrem **-SslCertFullPath**. |
| -StoreSystemAosUrl | Adresa URL centrály (AOS). |
| -StoreSystemChannelDatabaseId | ID databáze kanálů (název). |
| -TenantId | ID klienta Azure AD. |
| -TransactionServiceAzureAuthority | Autorita Azure AD transakční služby. |
| -TransactionServiceAzureResource | Zdroj Azure AD transakční služby. |
| -TrustSqlServerCertificate | Přepínač, který označuje, zda má být certifikát serveru důvěryhodný při navazování připojení k SQL Serveru. Aby se zabránilo bezpečnostním rizikům, produkční nasazení by zde nikdy neměla mít hodnotu **true**. Výchozí hodnota je **false**. |
| -Verbosity | Úroveň protokolování požadovaná během instalace. Obvykle by tato hodnota neměla být použita. |
| -WindowsPhoneAppInsightsInstrumentationKey | Klíč instrumentace hardwarové stanice AppInsights. |

## <a name="general-overview"></a>Obecný přehled

Nová architektura pro samoobslužné instalátory má různé funkce a vylepšení. Nová architektura v současné době generuje instalační programy pouze pro Modern POS, hardwarové stanice a CSU (v místním prostředí). Je důležité porozumět základnímu použití příkazového řádku v zapečetěných instalačních programech, které by mělo vypadat podobně jako v následujícím příkladu. 
 
```Console
<Component Installer Name>.exe install -<Parameter Name> "<Parameter Information>"
```

Instalační program vyžaduje parametr **install** (nebo **uninstall** k odebrání instalace) a všechny parametry specifické pro danou instalaci. **Název parametru** by měl zahrnovat všechny potřebné parametry, jako je pokladna, adresa URL CSU nebo informace o certifikátu. **Informace parametru** by měla obsahovat jakékoli další informace o parametrech.

Architektura zapečetěných instalačních programů byla vytvořena tak, aby umožňovala následující změny:
- **Zapečetěno** – Nová architektura instalačních programů zcela odděluje instalační programy základních komponent distribuované společností Microsoft od přizpůsobení založených na rozšiřitelnosti. Přizpůsobení budou nainstalována později, ale poté budou odpojena s ohledem na aktualizace (takže aktualizace budou povoleny pouze pro základní komponentu Microsoftu, pouze pro přizpůsobení, nebo pro obě části).
- **Bez GUI** – Již neexistuje uživatelské rozhraní (UI). Místo toho existuje pouze spustitelný soubor řízený příkazovým řádkem pro každý instalační program komponenty. Tato změna je jednou z několika klíčových změn nebo funkcí, které se používají k zaměření nové instalační architektury na použití s hromadným nasazením.
- **Podrobnější protokolování** – Vylepšené protokoly instalačního programu umožňují lepší ověření dokončení nebo selhání instalace, provedených kroků a všech vygenerovaných varování nebo chyb.
- **Čištění** – V nové architektuře se instalační programy komponent více zaměřují na udržování čistoty instalačních adresářů tím, že před instalací novějších komponent vyčistí celý obsah složky komponenty. Toto vyčištění zajistí, že ve složkách nezůstanou žádné soubory, které by mohly způsobit problémy a bránit úspěšné instalaci.

Do nové architektury nebyly migrovány tři komponenty: Virtual Peripheral Simulator, Async Server Connector Service (používá se k podpoře Dynamics AX 2012 R3) a Real-time Service Replacement (používá se k podpoře Dynamics AX 2012 R3).

> [!NOTE]
> Instalační programy jsou uloženy a uchovány lokálně.  Postupem času je důležité spravovat nebo odstraňovat zachované instalační programy, aby nedošlo k plýtvání místem na disku. Pro účely zotavení z extrémních situací se doporučuje ponechat aktuální instalační program pro základní součásti a instalační programy rozšíření pro nejnovější verze.

## <a name="migration"></a>Migrace

Migrace ze starých samoobslužných instalátorů komponent architektury na nové instalátory vyžaduje odinstalaci starých komponent.

- **Modern POS** – Nová architektura instalačních programů způsobila, že aplikace obdržela nové ID podpisu aplikace. Proto je před instalací komponenty Modern POS nové architektury vyžadována úplná odinstalace starých komponent. Kvůli požadavku na úplnou odinstalaci bude znovu vyžadována aktivace zařízení. (Tato reaktivace zařízení je jednorázový požadavek za předpokladu, že k odinstalaci již znovu nedojde.)
- **Hardwarová stanice** – Coby web IIS vyžaduje nová architektura instalačních programů přepracování základní struktury složek. Proto je před instalací komponenty hardwarové stanice nové architektury vyžadována úplná odinstalace starých komponent.
- **Commerce Scale Unit (CSU, v místním prostředí)** – Coby řada webů IIS vyžaduje nová architektura instalačních programů přepracování základní struktury složek.  Proto je před instalací komponenty CSU (v místním prostředí) nové architektury vyžadována úplná odinstalace starých komponent.

## <a name="modern-pos"></a>Modern POS

### <a name="before-you-begin"></a>Než začnete

Je důležité, abyste odstranili starou, samoobslužnou komponentu Modern POS. Více informací naleznete v předchozích krocích migrace v tomto článku.

> [!NOTE]
> V systému s jedním počítačem, jako je topologie vývojáře nebo demonstrační prostředí, nebo když jsou Commerce Scale Unit a Modern POS nainstalovány na stejném počítači, je možné, že Store Commerce nebude moci dokončit aktivaci zařízení. K tomuto problému dochází, protože Store Commerce nemůže provádět síťová volání do stejného počítače (tj. sama sebe). I když by to v produkčním nastavení nikdy nemělo být povoleno, problém lze zmírnit povolením výjimky zpětné smyčky AppContainer, aby komunikace mohla probíhat na stejném počítači. K dispozici jsou různé aplikace, pomáhající povolit tuto zpětnou smyčku. Další informace o nastavení zpětné smyčky naleznete v tématu [Jak povolit zpětnou smyčku a odstraňovat problémy s izolací sítě](/previous-versions/windows/apps/hh780593(v=win.10)). Je důležité pochopit, že zpětná smyčka může představovat bezpečnostní riziko, proto se nedoporučuje ji používat, pokud to není nezbytně nutné.

### <a name="examples-of-silent-deployment"></a>Příklady bezobslužného nasazení

Tato část ukazuje příklady příkazů, které se používají k instalaci Modern POS.

#### <a name="silently-install-modern-pos"></a>Bezobslužná instalace Modern POS

Následující příkaz bezobslužně nainstaluje (nebo aktualizuje) Modern POS. Má standardní strukturu příkazů, která se používá pro bezobslužnou údržbu komponent, které jsou aktuálně nainstalovány. Struktura využívá základní hodnoty ze souboru **&lt;NázevInstalátoru&gt;.exe**.

Následující základní příkaz ukazuje dostupné možnosti, pokud je požadována instalace. Důrazně doporučujeme použít tento příkaz při prvním testování nebo použití instalačního programu.

```Console
CommerceModernPOS.exe -help install
```

> [!NOTE]
> U Modern POS není vyžadován konfigurační soubor. Instalační program má nyní parametry (uvedené dříve v tomto článku) pro různé hodnoty, které se používají během aktivace zařízení.

Následující příkaz specifikuje všechny parametry, které by měly být použity během aktivace zařízení po instalaci aplikace Modern POS. Tento příklad používá pokladnu **Houston-3**, což je běžně používaná hodnota v ukázkových datech Dynamics 365 Commerce.

```Console
CommerceModernPOS.exe install -Register "Houston-3" -Device "Houston-3" -RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Následující příkaz určuje parametry, které by měly být použity k instalaci a konfiguraci offline databáze. SQL Server je specifikován spolu s konfiguračním souborem, který má být použit.

```Console
CommerceModernPOS.exe install -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

Tyto koncepty můžete kombinovat, abyste dosáhli požadovaných výsledků instalace.

## <a name="hardware-station"></a>Hardwarová stanice

### <a name="before-you-begin"></a>Než začnete

Je důležité, abyste odstranili starou samoobslužnou komponentu hardwarové stanice. Více informací naleznete v předchozích krocích migrace v tomto článku. Nástroj pro informace o účtu obchodníka již neexistuje. Místo toho se informace o účtu obchodníka nainstalují, když je terminál POS spárován s hardwarovou stanicí. Důrazně doporučujeme spustit následující příkaz při prvním testování instalačního programu.

```Console
CommerceHardwareStation.exe -help install
```

### <a name="examples-of-silent-deployment"></a>Příklady bezobslužného nasazení

Tato část ukazuje příklady příkazů, které se používají k instalaci hardwarové stanice.

#### <a name="silently-install-hardware-station"></a>Bezobslužná instalace hardwarové stanice

Následující příkaz bezobslužně nainstaluje (nebo aktualizuje) hardwarovou stanici. Má standardní strukturu příkazů, která se používá pro údržbu komponent, které jsou aktuálně nainstalovány. Struktura využívá základní hodnoty ze souboru **&lt;NázevInstalátoru&gt;.exe**.

Následující základní příkaz spustí instalační program spustitelného souboru.

```Console
HardwareStation.exe install -Port 443 -StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" -StoreSystemChannelDatabaseID "Houston" -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> U hardwarové stanice není vyžadován konfigurační soubor. Instalační program má nyní parametry (uvedené dříve v tomto článku) pro různé povinné hodnoty.

Následující příkaz uvádí všechny parametry, které jsou nutné k přeskočení kontrol nezbytných požadavků během standardní instalace. 

> [!NOTE]
> Přeskakování kontrol se nedoporučuje bez důkladného dopředného testování nebo ve vývojových scénářích.

```Console
HardwareStation.exe install -SkipFirewallUpdate -SkipOPOSCheck -SkipVersionCheck -SkipURLCheck -Config "HardwareStation.Houston.xml"
```

Jak je zvykem, je běžné tyto koncepty kombinovat, abyste dosáhli požadovaných výsledků instalace.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (v místním prostředí)

Důrazně doporučujeme spustit následující příkaz při prvním testování instalačního programu.

```Console
CommerceStoreScaleUnitSetup.exe -help install
```

### <a name="before-you-begin"></a>Než začnete

Je důležité, abyste odstranili starou, samoobslužnou komponentu CSU (v místním prostředí). Více informací naleznete v předchozích krocích migrace v tomto článku.

### <a name="examples-of-silent-deployment"></a>Příklady bezobslužného nasazení

Tato část ukazuje příklady příkazů, které se používají k instalaci CSU (v místním prostředí).

#### <a name="silently-install-csu-self-hosted"></a>Bezobslužná instalace CSU (v místním prostředí)

Následující příkaz bezobslužně nainstaluje (nebo aktualizuje) CSU (v místním prostředí). Má standardní strukturu příkazů, která se používá pro bezobslužnou údržbu komponent, které jsou aktuálně nainstalovány. Struktura využívá základní hodnoty ze souboru **&lt;NázevInstalátoru&gt;.exe**.

Ve srovnání s ostatními samoobslužnými instalátory je Commerce Scale Unit (CSU) složitější a vyžaduje poměrně velké množství dalších informací. Následující příkaz je minimální příkaz (s parametry) potřebný ke spuštění instalačního programu spustitelného souboru, když není přítomen žádný konfigurační soubor.

```Console
CommerceScaleUnit.exe install -port 446 -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> U CSU (v místním prostředí) je stále vyžadován konfigurační soubor.

Následující příkaz je podrobnějším příkazem, který spustí instalační program spustitelného souboru s některými alternativními parametry.

```Console
CommerceScaleUnit.exe install -Port 446 -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Verbosity 0 -Config "Contoso.StoreSystemSetup.xml"
```

Následující příkaz uvádí parametry, které jsou nutné k přeskočení kontrol nezbytných požadavků během standardní instalace. 

> [!NOTE]
> Přeskakování kontrol se nedoporučuje bez důkladného dopředného testování nebo ve vývojových scénářích.


```Console
CommerceScaleUnit.exe installer -skipscaleunithealthcheck -skipcertcheck -skipaadcredentialscheck -skipschannelcheck -skipiischeck -skipnetcorebundlecheck -skipsqlservercheck -skipnetframeworkcheck -skipversioncheck -skipurlcheck -Config "Contoso.StoreSystemSetup.xml" -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate
```

Tyto koncepty můžete kombinovat, abyste dosáhli požadovaných výsledků instalace.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
