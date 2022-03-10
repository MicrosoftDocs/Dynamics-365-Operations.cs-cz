---
title: Nastavení přímé integrace italské elektronické faktury FatturaPA s SDI
description: Toto téma poskytuje informace, které vám pomohou začít s elektronickou fakturací pro Itálii a nastavit přímou integraci italské elektronické faktury FatturaPA se systémem Exchange (SDI).
author: abaryshnikov
ms.date: 01/15/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 73cb08c880d7b3459201acfc7aeaa8d0dee1674f
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984796"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Nastavení přímé integrace italské elektronické faktury FatturaPA s SDI

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Elektronická fakturace pro Itálii nemusí aktuálně podporovat všechny funkce, které jsou k dispozici pro elektronické faktury v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.

Toto téma poskytuje informace, které vám pomohou začít s elektronickou fakturací pro Itálii v aplikacích Finance a Supply Chain Management. Provede vás konfiguračními kroky, které jsou závislé na zemi/oblasti v Regulatory Configuration Services (RCS). Tyto kroky doplňují kroky popsané v části [Začínáme s elektronickou fakturací](e-invoicing-get-started.md).

## <a name="prerequisites"></a>Předpoklady

Před provedením kroků v tomto tématu musí být splněny následující předpoklady:

- Proveďte kroky v části [Začínáme s elektronickou fakturací](e-invoicing-get-started.md).
- Z globálního úložiště importujte funkci elektronické fakturace **Italská elektronická faktura FatturaPA (IT)** do RCS. Více informací naleznete v sekci [Import funkce elektronické fakturace od poskytovatele konfigurace společnosti Microsoft](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) ve výše uvedeném tématu „Začínáme s elektronickou fakturací“.
- Do prostředí služby přidejte odkazy z požadovaných certifikátů. Mezi požadované certifikáty patří certifikát digitálního podpisu, certifikát certifikační autority (CA) a klientský certifikát. Další informace viz sekce [Vytvoření tajného klíče digitálního certifikátu](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) v části „Začínáme se správou služby elektronické fakturace“.

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Konfigurace funkce elektronické fakturace Italská elektronická faktura FatturaPA (IT) závislé na zemi

Před nasazením nastavení aplikace do připojené aplikace Finance nebo Supply Chain Management proveďte následující kroky.

Tato sekce doplňuje sekci [Konfigurace nastavení aplikace specifická pro zemi](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) v tématu „Začínáme s Elektronickou fakturací“.

### <a name="create-a-new-feature"></a>Vytvoření nové funkce

1. Přihlaste se do RCS.
2. V pracovním prostoru **Elektronické výkaznictví** v sekci **Poskytovatelé konfigurace** označte poskytovatele konfigurace vaší společnosti jako aktivního.
3. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **Elektronická fakturace**.
4. Na stránce **Funkce elektronické fakturace** vyberte **Přidat** \> **Na základě stávající funkce**.
5. V sekci **Poskytovatel konfigurace společnosti Microsoft** vyberte **Italská elektronická faktura FatturaPA (IT)** jako základní funkci, zadejte název a poté vyberte **Vytvořit funkci**.

### <a name="set-up-application-specific-parameters"></a>Nastavení parametrů pro konkrétní aplikaci

1. Na stránce **Funkce elektronické fakturace** vyberte funkci, abyste ji mohli upravit.
2. Na kartě **Verze** ověřte, že je vybrána verze **Koncept**.
3. Na kartě **Konfigurace** vyberte konfiguraci a poté vyberte **Specifické parametry aplikace**.
4. V sekci **Vyhledávání** se ujistěte, že je vybráno vyhledávání **Seznam podkategorií přenesení daňové povinnosti Natura**.
5. V sekci **Podmínky** vyberte **Přidat**.
6. Přidejte specifické podmínky pro každou podkategorii, která je definována v systému, a poté uložte změny.

    > [!NOTE]
    > Ve sloupci **Název** můžete vybrat hodnotu zástupného symbolu **\*Prázdné\*** nebo **\*Není prázdné\*** namísto konkrétní hodnoty.

### <a name="configure-a-processing-pipeline-for-export"></a>Konfigurace zpracování kanálu pro export

1. Na stránce **Funkce elektronické fakturace** vyberte funkci, abyste ji mohli upravit.
2. Na kartě **Nastavení** vyberte **Prodejní faktury** a poté vyberte **Upravit**.
3. V sekci **Zpracování kanálu** projděte část s akcemi a nastavte všechna požadovaná pole:

    - Pro akci **Podepsat dokument** v poli **Název certifikátu** zadejte certifikát digitálního podpisu.
    - Pro akci **Odeslat** nastavte pole **Adresa URL** a **Certifikáty**. Hodnota pole **Certifikáty** je řetěz certifikátů, z nichž první je kořenový certifikát CA (caentrate.cer) a druhý je certifikát klienta.

4. Vyberte **Ověřit**, abyste se ujistili, že byla nastavena všechna požadovaná pole.
5. Uložte změny a zavřete stránku.
6. Na kartě **Nastavení** vyberte **Projektové faktury** a poté vyberte **Upravit**.
7. Opakujte kroky 3 až 5 pro projektové faktury.

### <a name="configure-the-processing-pipeline-for-import"></a>Konfigurace zpracování kanálu pro import

1. Na stránce **Funkce elektronické fakturace** vyberte funkci, abyste ji mohli upravit.
2. Na kartě **Nastavení** vyberte **Importovat faktury** a poté vyberte **Upravit**.
3. V sekci **Datový kanál** na kartě **Parametry** v poli **Datový kanál** zadejte hodnotu řetězce.
4. Na kartě **Pravidla použitelnosti** nastavte pole pro nastavení. Můžete použít výchozí klauzuli **Kanál** předáním hodnoty, kterou jste nastavili pro pole **Datový kanál** v předchozím kroku, do pole **Hodnota**.

    ![Nastavení pravidel použitelnosti.](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Vyberte **Ověřit**, abyste se ujistili, že byla nastavena všechna požadovaná pole.

### <a name="deploy-the-feature"></a>Nasazení funkce

1. Dokončete, publikujte nebo nasaďte funkci prostředí služby. Další informace viz sekce [Nasazení funkce elektronické fakturace do prostředí služby](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) v tématu „Začínáme s elektronickým fakturovánímׅ“.
2. Nasazení funkce připojené aplikace. Další informace viz sekce [Nasazení funkce elektronické fakturace do připojené aplikace](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) v tématu „Začínáme s elektronickým fakturovánímׅ“.

### <a name="set-up-finance"></a>Nastavení aplikace Finance

1. Přihlaste se k prostředí Finance.
2. V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft**.
3. Vyberte **Úložiště** \> **Globální** \> **Otevřít**.
4. Vyberte a importujte konfigurace **Model kontextu faktury odběratele** a **Import faktury dodavatele (IT)**.
5. Přejděte na **Správa organizace** \> **Nastavení** \> **Parametry elektronického dokumentu**.
6. Na kartě **Funkce** vyhledejte a vyberte funkci **Italská elektronická faktura** a poté zaškrtněte políčko **Povolit**.
7. Na kartě **Elektronický dokument** se ujistěte, že pole pro **Deník faktur odběratele** a **Projektová faktura** jsou nastaveny podle postupu v sekci [Konfigurace nastavení aplikace](e-invoicing-get-started.md#configure-the-application-setup).

### <a name="set-up-vendor-invoice-import"></a>Nastavení importu faktur dodavatele 

1. V aplikaci Finance v pracovním prostoru **Elektronické výkaznictví** v sekci **Poskytovatelé konfigurace** označte poskytovatele konfigurace vaší společnosti jako aktivního.
2. Vyberte **Konfigurace vykazování**.
3. Vyberte **Model kontextu faktury odběratele** a poté vyberte **Vytvořit konfiguraci**.
4. Vyberte **Odvodit z názvu: Model kontextu faktury odběratele**, čímž vytvoříte odvozenou konfiguraci.
5. Ve verzi **Koncept** vyberte **Návrhář**.
6. Ve stromě **Datový model** vyberte **Mapovat model na datový zdroj**.
7. Ve stromu **Definice** vyberte **DataChannel** a poté vyberte **Návrhář**.
8. Ve stromu **Zdroje dat** rozbalte kontejner **\$Context\_Channel**.
9. V poli **Hodnota** vyberte **Upravit**. 
10. Zadejte název datového kanálu. Název může mít maximálně 10 znaků. Měl by odpovídat hodnotě parametru **Datový kanál** datového kanálu pro funkci elektronické fakturace v RCS.
11. Uložte změny a přejděte na **Konfigurace výkaznictví** \> **Kompletní verze konfigurace**.
12. Na kartě **Externí kanály** v sekci **Kanály** vyberte **Přidat**.
13. V pole **Kanál** zadejte hodnotu **\$Kontextový kanál**.
14. Zadejte hodnoty do polí **Popis** a **Společnost**.
15. V poli **Kontext dokumentu** vyberte novou konfiguraci, kterou jste odvodili od **Modelu kontextu faktury odběratele**. Popis mapování by měl být **Kontext datového kanálu**.
16. Na kartě **Import zdrojů** vyberte možnost **Přidat** a nastavte následující hodnoty:

    - **Název:** OutputFile
    - **Název datové entity:** Záhlaví faktury dodavatele (**Datová entita:** VendorInvoiceHeaderEntity)
    - **Mapování modelu:** Import faktury dodavatele (IT)

> [!NOTE]
> Pokud importujete faktury dodavatele z různých zdrojů, můžete vytvořit několik externích kanálů a několik odvozených konfigurací, které mají jiné hodnoty **\$Kontextového kanálu**. Můžete chtít například importovat faktury dodavatele pro různé právnické osoby.

## <a name="proxy-server-setup"></a>Nastavení proxy serveru

Tato sekce obsahuje informace, které vám pomohou nastavit a nakonfigurovat službu proxy pro komunikaci mezi systémem Exchange (SDI) a službou elektronické fakturace.

### <a name="create-an-app-registration"></a>Vytvoření registrace aplikace

1. Pomocí následujícího skriptu Windows PowerShell vytvořte certifikát podepsaný svým držitelem (self-signed certificate) pro ověřování typu service-to-service (S2S).

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. Uložte soubor certifikátu .pfx do trezoru klíčů a poté odstraňte místní kopii.
3. Přihlaste se k [Azure Portal](https://portal.azure.com) jako správce.
4. Vytvořte registraci aplikace pro službu SDI Proxy.

    1. Přejděte na **Registrace aplikací**, vytvořte registraci a poté pro ni nastavte následující hodnoty:

        - **Název:** Proxy klient SDI
        - **Podporované typy účtů:** Účty pouze v tomto organizačním adresáři (jeden klient)

    2. Vyberte **Registrovat** a poté vyberte registraci aplikace, kterou jste právě vytvořili.
    3. Jděte na **Oprávnění API** a vyberte **Udělit souhlas správce**.
    4. Jděte na **Certifikáty a tajné klíče**, vyberte **Nahrát certifikát** a nahrajte soubor certifikátu .cer pro ověřování S2S.
    5. Jděte na **Podnikové aplikace** a vyberte aplikaci, kterou jste vytvořili.
    6. Uložte hodnoty **ID aplikace** (ID klienta) a **ID objektu** náležící aplikaci.
    7. Tým pro službu fakturace musí aplikaci udělit přístup ke službě. Odešlete hodnoty následujících parametrů na adresu <D365EInvoiceSupport@microsoft.com>:

        - ID klienta AAD
        - ID prostředí LCS
        - ID aplikace
        - ID objektu

5. V RCS přidejte aplikaci do seznamu aplikací vašeho prostředí služby.

    1. Jděte na **Funkce globalizace** \> **Prostředí** \> **Elektronická fakturace** \> **Prostředí služeb** a vyberte své prostředí.
    2. V sekci **Aplikace** přidejte řádek do mřížky a zadejte název a ID objektu aplikace.

        ![Přidání aplikace do prostředí služby.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Vyberte **Uložit** a potom **Publikovat**.

### <a name="create-an-azure-virtual-machine"></a>Vytvoření virtuálního počítače Azure

1. V portálu Azure přejděte na [Azure Portal](https://portal.azure.com), jděte na **Virtuální počítače** a vyberte **Vytvořit nový**.
2. Na kartě **Základy** vyberte své předplatné a skupinu prostředků. Hodnoty musí být předplatné a skupina prostředků, kde se nachází váš trezor klíčů a úložiště objektů BLOB.
3. Vyberte oblast. Tato hodnota musí být oblast, kde je nasazeno vaše prostředí Finance.
4. Přidejte uživatelské jméno a heslo správce a uložte je do trezoru klíčů.
5. V poli **Vyberte porty pro příchozí spojení** vyberte **HTTPS (443)** a **RPD (3389)**.

    > [!NOTE]
    > Doporučujeme deaktivovat port **RDP (3389)**, když systém přejde do výroby. Můžete jej znovu povolit, pokud se kvůli odstraňování problémů budete muset připojit k virtuálnímu počítači (VM).

    ![Nastavení polí na kartě Základy pro vytvoření virtuálního počítače Azure.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Na kartě **Disky** na záložce s náhledem **Rozšířené** zaškrtněte políčko **Používat spravované disky**. Zaškrtávací políčko **Dočasný disk s operačním systémem** ponechte nezaškrtnuté.

    ![Nastavení polí na kartě Disky pro vytvoření virtuálního počítače Azure.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. Na kartě **Sítě** pod polem **Veřejná IP adresa** vyberte **Vytvořit novou**.

    ![Nastavení polí na kartě Sítě pro vytvoření virtuálního počítače Azure.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. V dialogovém okně **Vytvoření veřejné IP adresy** ve skupině polí **SKU** vyberte možnost **Standardní**. Ve skupině polí **Přiřazení** vyberte možnost **Statické**.

    ![Vytvoření veřejné IP adresy.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. Na kartě **Správa** vymažte zaškrtávací políčko **Automatické vypnutí**, čímž zakážete automatické vypnutí.
10. Nastavte pole **Aktualizace hostujícího OS** na **Ručně** a poté nastavte další zásady.
11. Kontrola a vytvoření virtuálního počítače.
12. V novém virtuálním počítači přejděte na **Identita** \> **Přiřazeno systémem** a nastavte možnost **Stav** jako **Zapnuto**.
13. Udělení přístupu virtuálního počítače k trezoru klíčů.

    1. V trezoru klíčů přejděte na **Řízení přístupu (IAM)** \> **Přiřazení rolí**.
    2. Vyberte **Přidat přiřazení role** a poté nastavte následující pole:

        1. V poli **Role** zadejte **Uživatel tajných klíčů z trezoru klíčů**.
        2. V poli **Přiřadit přístup k** zadejte **Virtuální počítač**.
        3. V poli **Předplatné** zadejte své předplatné.
        4. V poli **Vybrat** zadejte svůj virtuální počítač.

    3. Přejděte na **Zásady přístupu**.
    4. Vyberte **Přidat zásady přístupu** a poté nastavte následující pole:

        1. V poli **Vybraný objekt zabezpečení** vyberte svůj virtuální počítač.
        2. V sekci **Certifikát** vyberte oprávnění **Seznam** a **Získat**.

14. V [Azure Portal](https://portal.azure.com) jděte na **Veřejné IP adresy** a vyberte IP adresu, která byla vytvořena ve virtuálním počítači.
15. Jděte do **Konfigurace** a nastavte název DNS (Domain Name System).

### <a name="prepare-the-proxy-service-environment"></a>Příprava prostředí služby proxy

Na počítači, kde je hostována služba proxy, postupujte takto.

1. Připojte se k virtuálnímu počítači pomocí připojení ke vzdálené ploše.
2. Otevřete modul snap-in Certifikát místního počítače. Další informace viz [Návod: Zobrazení certifikátů pomocí modulu snap-in konzoly MMC](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in).
3. Importujte certifikát **caentrate.cer** pro výrobu a certifikát **CAEntratetest.cer** pro testování do [úložiště důvěryhodné kořenové certifikační autority](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores). (**CAEntratetest.cer** je certifikát kořenové CA, který poskytl úřad.)
4. V ovládacích panelech otevřete **Zapnout nebo vypnout funkce Windows** nebo přejděte na **Správce serveru** \> **Přidat role a funkce** pro serverový operační systém (OS) a zapněte funkce internetové informační služby (IIS):

    - Nástroje webové správy
        - Konzola pro správu služby IIS
    - Webové služby
        - Funkce pro vývoj aplikací
            - Rozšiřitelnost rozhraní .NET 4.7 (nebo 4.8)
            - ASP
            - ASP.NET 4.7 (nebo 4.8)
            - CGI
            - Rozšíření ISAPI
            - Filtry ISAPI
        - Společné funkce protokolu HTTP
            - Výchozí dokument
            - Procházení adresářů
            - Chyby protokolu HTTP
            - Statický obsah
        - Stav a diagnostika
            - Protokolování protokolu HTTP
            - Sledování
        - Funkce výkonu
            - Komprese statického obsahu
        - Zabezpečení
            - Filtrování žádostí

    ![Zapnutí funkcí ISS.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>Nastavení služby SDI Proxy ve službě IIS

1. Ve službě Microsoft Dynamics Lifecycle Services (LCS) otevřete knihovnu sdíleného majetku a jako typ majetku vyberte **Datový balíček**.
2. Vyhledejte **SDI Proxy služby elektronické fakturace** a stáhněte si jej do virtuálního počítače.
3. Konfigurace služby.

    1. Rozbalte složku archivu **SDI Proxy služby elektronické fakturace**, kterou jste si stáhli.
    2. Ve složce **src\\FattureService** otevřete soubor **appsettings.json** a nastavte následující parametry:

        - **KeyVaultUri** – Zadejte adresu trezoru klíčů, ve kterém je uložen klientský certifikát pro fakturační službu.
        - **TenantId** – Zadejte globálně jedinečný identifikátor (GUID) klienta zákazníka.
        - **EnvironmentId** – Zadejte ID prostředí LCS.
        - **ClientId** – Zadejte ID registrace aplikace zprostředkujících služeb v klientovi zákazníka.
        - **ClientCertificateName** – Zadejte název certifikátu S2S v trezoru klíčů.
        - **SecurityServiceClientOptions.Endpoint** – Zadejte adresu URL bezpečnostní služby.
        - **SecurityServiceClientOptions.Resource** – Zadejte rozsah, pro který chcete získat token.
        - **InvoicingServiceClientOptions.Endpoint** – Zadejte koncový bod fakturační služby. Tato hodnota musí být stejný koncový bod, který se používá pro RCS a Finance.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – Zadejte název prostředí služby. Tato hodnota musí být název vašeho prostředí Finance.
        - **NotificationsFolder** – Určete složku, do které se mají ukládat soubory příchozích oznámení.

    3. V souboru **web.config** vyhledejte následující řádek a přidejte miniaturu certifikátu proxy serveru.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Když systém přejde do výroby, můžete změnit některé hodnoty v souboru web.config, abyste snížili množství shromažďovaných informací protokolu a pomohli ušetřit místo na disku. V uzlu **\<system.diagnostics\>\<source\>** změňte hodnotu **switchValue** na **Critical.Error**. Další informace naleznete v tématu [Prohlížeč trasování služby MS](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).

4. Otevřete správce služby IIS. Ve stromu nalevo zůstaňte v kořenovém uzlu. Vpravo vyberte **Certifikáty serveru**.

    ![Výběr certifikátů služby ve správci služby IIS.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Otevřete nabídku a vyberte **Importovat**.
6. V dialogovém okně **Import certifikátu** v poli **Soubor certifikátu (.pfx)** zadejte cestu k souboru .pfx pro certifikát proxy serveru.

    ![Určení souboru certifikátu služby proxy.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Vyberte a podržte (nebo klikněte pravým tlačítkem) na možnosti **Weby** a vyberte možnost **Přidat weby**.
8. V dialogovém okně **Přidání webu** zadejte v poli **Název webu** jedinečný název webu.
9. V poli **Fyzická cesta** ukažte na složku **src\\FattureService**.
10. V poli **Typ vazby** vyberte možnost **https**.
11. V poli **Název hostitele** zadejte název hostitele.
12. Pole **IP adresa** a **Port** ponechte nastavena na výchozí hodnoty.
13. Ujistěte se, že je vymazáno políčko **Vyžaduje indikaci názvu serveru**, protože SDI tuto technologii nepodporuje.
14. V poli **Certifikát protokolu SSL** vyberte certifikát serveru proxy, který jste importovali.
15. V poli **Fond aplikací** zadejte fond pro web a poznamenejte si jeho název (např. **SdiAppPool**).

    ![Přidání webu.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Po vytvoření webu otevřete nabídku pro **Nastavení protokolu SSL**.

    ![Otevření nabídky pro nastavení protokolu SSL.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Zaškrtněte políčko **Vyžaduje protokol SSL** a poté ve skupině polí **Klientské certifikáty** vyberte možnost **Vyžaduje**.

    ![Konfigurace nastavení protokolu SSL.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Otevřete **Procházení adresářů** a vyberte možnost **Povolit**.
19. V libovolném webovém prohlížeči přejděte na **serverDNS/TrasmissioneFatture.svc**. Musí se zobrazit standardní stránka o službě.

    ![Kontrola služby v prohlížeči.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Vytvořte následující složky pro uchovávání protokolů a souborů:

    - **C:\\Logs\\** – Zde ukládejte soubory protokolu. Tyto soubory lze prohlížet pomocí [prohlížeče trasování služby MS](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).
    - **C:\\Files\\** – Zde uchovávejte všechny soubory odpovědí.

21. V Průzkumníku souborů udělte přístup **SÍŤOVÁ SLUŽBA** a **IIS AppPool\\SdiAppPool** (nebo **IIS AppPool\\DefaultAppPool**, pokud používáte výchozí fond) ke složkám **Logs** a **Files**.

    1. Vyberte a podržte (nebo klikněte pravým tlačítkem) na jedné ze složek a vyberte možnost **Vlastnosti**.
    2. V dialogovém okně **Vlastnosti** na kartě **Zabezpečení** vyberte **Upravit**.
    3. Přidejte uživatele, pokud zde nejsou uvedeni.
    4. Zopakujte kroky 1 až 3 pro druhou složku.

    ![Přidání oprávnění uživateli služby.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů 

Povolení funkce **Italská elektronická faktura** může vyžadovat odesílání omezeného objemu dat. Tato data zahrnují identifikační daňové identifikační číslo organizace. Správce může aktivovat a deaktivovat funkci italské elektronické faktury. Pokud chcete zakázat tuto funkci, postupujte takto.

1. Přejděte na **Správa organizace** \> **Nastavení** \> **Parametry elektronického dokumentu**.
2. Na kartě **Funkce** vyberte řádek obsahující funkci **Italská elektronická faktura** a poté vyberte **Zakázat**.

Data importovaná z těchto externích systémů do této online služby Dynamics 365 podléhají našim [Prohlášením o ochraně osobních informací](https://go.microsoft.com/fwlink/?LinkId=512132). Další informace najdete v sekci Oznámení o ochraně osobních údajů v dokumentaci funkcí pro jednotlivé země/oblasti.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronické fakturace](e-invoicing-service-overview.md)
- [Začínáme se správou služby Elektronické fakturace](e-invoicing-get-started-service-administration.md)
- [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
