---
title: Domény v Dynamics 365 Commerce
description: Tohle téma popisuje, jak se zachází s doménami v Microsoft Dynamics 365 Commerce.
author: BrShoo
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 8d4381c64b69f8b62dcb509407c4f04dcee696ae
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792792"
---
# <a name="domains-in-dynamics-365-commerce"></a>Domény v Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Tohle téma popisuje, jak se zachází s doménami v Microsoft Dynamics 365 Commerce.

Domény jsou webové adresy používané k navigaci na weby Dynamics 365 Commerce ve webovém prohlížeči. Správu své domény provádíte u vybraného poskytovatele serveru DNS (Domain Name Server). Na domény se odkazuje v rámci konfigurátoru webů Dynamics 365 Commerce za účelem koordinace přístupu na web, když je publikován. Toto téma popisuje, jak se s doménami zachází a jak se na ně odkazuje během celého životního cyklu vývoje a spuštění webu Commerce.

## <a name="provisioning-and-supported-host-names"></a>Zřizování a podporované názvy hostitelů

Při zřizování prostředí elektronického obchodu v [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), pole **Podporované názvy hostitelů** na obrazovce zřizování elektronického obchodu se používá k zadání domén, které budou přidruženy k nasazenému prostředí Commerce. Tyto domény budou názvy zákaznických serverů DNS (Domain Name Server), na kterých budou hostovány weby elektronických obchodů. Zadání domény v této fázi nepřesměruje provoz domény na Dynamics 365 Commerce. Provoz domény bude směrován pouze do koncového bodu Commerce, když se aktualizuje záznam DNS CNAME, aby se s doménou použil koncový bod Commerce.

> [!NOTE]
> Do pole **Podporované názvy hostitelů** můžete zadat více domén oddělených středníky.

Následující obrázek ukazuje obrazovku pro zřízení elektronického obchodu LCS se zvýrazněným polem **Podporované názvy hostitelů**. 

![Obrazovka pro zřízení elektronického obchodu LCS se zvýrazněným polem **Podporované názvy hostitelů**](./media/Domains_ProvisioningeCommerceScreen_publish.png)

Pokud již došlo ke zřízení, můžete vytvořit požadavek na službu a přidat do prostředí další domény. Chcete-li vytvořit požadavek na službu v LCS, přejděte ve svém prostředí na **Podpora \> Problémy s podporou** a vyberte **Odeslat incident**.

## <a name="commerce-generated-urls"></a>Adresy URL generované řešením Commerce

Při zřizování prostředí elektronického obchodu Dynamics 365 Commerce vygeneruje Commerce adresu URL, která bude pracovní adresou prostředí. Tuto adresu URL obsahuje odkaz na web elektronického obchodu zobrazeném v LCS po zřízení prostředí. Adresa URL generovaná řešením Comerce je ve formátu `https://<e-commerce tenant name>.commerce.dynamics.com`, kde název klienta elektronického obchodu je název zadaný v LCS pro prostředí Commerce.

Můžete také použít názvy hostitelů výrobního webu v prostředí sandbox. Tato možnost je ideální, když budete kopírovat web z prostředí sandbox do produkčního prostředí.

## <a name="site-setup"></a>Nastavení webu

Po zřízení prostředí elektronického obchodu musíte nastavit svůj web v konfigurátoru webů Commerce a přidružit jej k pracovní adrese URL.

Při prvním nastavení webu v konfigurátoru webů se zobrazí dialogové okno **Nastavte svůj web**.

Následující obrázek ukazuje dialogové okno **Nastavte svůj web** pro web s názvem „výchozí“ při prvním přístupu na web v konfigurátoru webů.

![Dialogové okno **Nastavte svůj web**](./media/Domains_SetupyoursiteScreen.png)

Pole **Vyberte doménu** umožňuje přidružit jeden z podporovaných názvů hostitelů poskytnutých pro váš web v LCS k vašemu webu v konfigurátoru webů.

Pole **Cesta** může zůstat prázdné nebo lze přidat další řetězec cesty, který se projeví ve vaší pracovní adrese URL. Při nevyplnění pole **Cesta** dojde k přidružení základní adresy URL generované řešením Commerce k webu nastavovaném v konfigurátoru webů. Cesty musí být pro každý pár web/doména jedinečná. V rámci vybraného webu a domény může pouze jeden web v prostředí použít prázdnou cestu nebo být přidružen k jedinečnému řetězci cesty. Libovolný řetězec přidaný do pole **Cesta** během nastavení webu se stane dílčí cestou základní adresy URL generované řešením Commerce, která se používá k přístupu na web ve webovém prohlížeči.

> [!NOTE]
> Cesta je také známá jako **Cesta pro párování** při přidávání kanálu do sekce konfigurace **Nastavení webu \> Kanály** v konfigurátoru webů.

Například pokud máte web v konfigurátoru webů s názvem „fabrikam“ v klientu elektronického obchodu s názvem „xyz“ a pokud nastavíte web s prázdnou cestou, měli byste přístup k publikovanému obsahu webu ve webovém prohlížeči přímým přechodem na základní adresu URL generovanou řešením Commerce:

`https://xyz.commerce.dynamics.com`

Alternativně, pokud byste během nastavení stejného webu přidali cestu „fabrikam“, měli byste přístup k publikovanému obsahu webu ve webovém prohlížeči pomocí následující adresy URL:

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a>Stránky a adresy URL

Jakmile má váš web nastavenu cestu, všechny adresy URL přidružené ke stránkám v konfigurátoru webů budou vycházet z funkční adresy URL (adresa generovaná řešením Commerce nebo adresa generovaná řešením Commerce plus cesta) pro daný web. Vytvoření nové adresy URL v konfigurátoru webů (**URLS /> + Nová**) výběrem stránky ze seznamu v dialogovém okně **Nová adresa URL** a zadání cesty URL pro tuto stránku přidruží tuto adresu URL k vybrané stránce. Hodnota cesty URL se poté připojí k pracovní adrese URL webu pro přístup na stránku a je označena jako `./<URL path>` v seznamu adres URL na stránce **Adresy URL** v konfigurátoru webů.

Následující obrázek ukazuje dialogové okno **Nová adresa URL** v konfigurátoru webů se zvýrazněnou ukázkovou adresou URL. 

![Dialogové okno **Nová adresa URL** v konfigurátoru webů](./media/Domains_PageSetup2a.png)

Následující obrázek ukazuje stránku **Adresy URL** v konfigurátoru webů se zvýrazněnou adresou URL v seznamu.

![Možnost Spustit tok uživatele v toku zásady](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Domény v konfigurátoru webů

Podporované hodnoty názvů hostitelů jsou k dispozici k přidružení jako doména při nastavování webu. Když vyberete hodnotu podporovaného názvu hostitele jako doménu, uvidíte vybranou doménu odkazovanou v celém konfigurátoru webů. Tato doména je pouze odkazem v prostředí Commerce, živý provoz pro tuto doménu ještě nebude přeposlán do Dynamics 365 Commerce.

Pokud při práci s weby v konfigurátoru webů máte dva weby nastavené se dvěma různými doménami, můžete připojit atribut **?domain=** k vaší pracovní adrese URL pro přístup k publikovanému obsahu webu v prohlížeči.

Například bylo zřízeno prostředí „xyz“ a v konfigurátoru webů byly vytvořeny a přidruženy dva weby: jeden s doménou `www.fabrikam.com` a druhý s doménou `www.constoso.com`. Každý web byl nastaven s prázdnou cestou. K těmto dvěma webům je pak možné přistupovat ve webovém prohlížeči pomocí atributu **?doména=**:
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

Pokud není řetězec dotazu na doménu zadán v prostředí s více doménami, použije Commerce první doménu, kterou jste zadali. Například pokud byla cesta „fabrikam“ poprvé zadána během nastavení webu, adresu URL `https://xyz.commerce.dynamics.com` lze použít pro přístup k publikovanému obsahu webu pro `www.fabrikam.com`.

## <a name="traffic-forwarding-in-production"></a>Přesměrování provozu ve výrobě

Můžete simulovat více domén pomocí parametrů řetězce dotazu na doménu na samotném koncovém bodě commerce.dynamics.com. Ale pokud potřebujete začít fungovat ve výrobě, musíte přesměrovat provoz pro vlastní doménu na koncový bod `<e-commerce tenant name>.commerce.dynamics.com`.

Koncový bod `<e-commerce tenant name>.commerce.dynamics.com` nepodporuje vlastní domény Secure Sockets Layers (SSL), takže musíte nastavit vlastní domény pomocí služby front door nebo sítě pro doručování obsahu (CDN). 

Chcete-li nastavit vlastní domény pomocí služby front door nebo CDN, máte dvě možnosti:

- Nastavit službu front door, jako je Azure Front Door, pro zpracování front-endu provozu a připojení k vašemu prostředí Commerce. To poskytuje větší kontrolu nad správou domén a certifikátů a podrobnější zásady zabezpečení.
- Použít instanci Azure Front Door poskytnutou řešením Commerce. To vyžaduje koordinační akci s týmem Dynamics 365 Commerce pro ověření domény a získání certifikátů SSL pro vaši doménu výroby.

Informace, jak přímo nastavit službu CDN, najdete v části [Přidání podpory pro síť pro doručování obsahu (CDN)](add-cdn-support.md).

Chcete-li použít instanci Azure Front Door poskytnutou řešením Commerce, musíte vytvořit požadavek na službu pomoci s instalací CDN od týmu pro zprovoznění řešení Commerce. 

- Budete muset zadat název vaší společnosti, doménu výroby, ID prostředí a název klienta elektronického obchodu výroby. 
- Budete muset potvrdit, zda se jedná o existující doménu (použitou se pro aktuálně aktivní web) nebo o novou doménu. 
- U nové domény lze ověření domény a certifikátu SSL dosáhnout v jediném kroku. 
- Pro doménu obsluhující existující webovou stránku je k vytvoření ověření domény a certifikátu SSL vyžadován vícestupňový proces. Tento proces má smlouvu o rozsahu služeb (SLA) na 7 dní pro zprovoznění domény, protože zahrnuje několik postupných kroků.

Chcete-li vytvořit požadavek na službu v LCS, přejděte ve svém prostředí na **Podpora \> Problémy s podporou** a vyberte **Odeslat incident**.

> [!NOTE]
> Vlastní domény s SSL jsou podporovány pouze v provozních prostředích. V neprovozních prostředích, jako je prostředí sandbox a testování přijetí uživatele (UAT), použijte URL generovanou řešením Commerce pro přístup k publikovanému obsahu ve webovém prohlížeči.

## <a name="ssl-certificate-process"></a>Proces certifikátu SSL

Když je podána žádost o službu, tým Commerce s vámi koordinuje následující kroky.

Pro nové domény:
- Tým Commerce nastaví instanci Azure Front Door (hostovaná v Commerce).
- Tým Commerce poté poskytne záznam CNAME k ukázání na vaší vlastní doménu.
- Po aktualizaci záznamu CNAME bude instance Azure Front Door hostovaná v Commerce moci ověřit vlastnictví domény a získat certifikát SSL.

Pro existující/aktivní domény:
- Tým Commerce vám dá pokyn, abyste přidali záznam CNAME `afdverify.<custom-domain>`, který poskytnete poskytovateli DNS vaší domény.
- Po dokončení tým Commerce přidá doménu do instance Azure Front Door a poskytne další záznamy DNS TXT, které se mají přidat do DNS pro doménu.
- Po dokončení záznamů TXT tým Commerce dokončí aktualizace Azure Front Door pro doménu, která nastaví certifikát SSL.

## <a name="apex-domains"></a>Vrcholové domény

Instance Azure Front Door poskytnutá řešením Commerce nepodporuje vrcholové domény (kořenové domény, které neobsahují subdomény). Vrcholové domény vyžadují k rozlišení IP adresu a instance Commerce Azure Front Door existuje pouze s virtuálními koncovými body. Chcete-li použít vrcholovou doménu, máte dvě možnosti:

- **Možnost 1** – Použijte poskytovatele DNS k přesměrování vrcholové domény na doménu „www“. Například fabrikam.com přesměruje na `www.fabrikam.com`, kde `www.fabrikam.com` je záznam CNAME, který odkazuje na instanci Azure Front Door hostovanou řešením Commerce.

- **Možnost 2** – Vytvořte vlastní instanci CDN / front door pro hostování vrcholové domény.

> [!NOTE]
> Pokud používáte Azure Front Door, musíte také nastavit Azure DNS ve stejném předplatném. Vrcholová doména hostovaná na Azure DNS může odkazovat na vaše Azure Front Door jako aliasový záznam. Toto je jediné řešení, protože vrcholové domény musí vždy ukazovat na IP adresu.

  ## <a name="additional-resources"></a>Další prostředky

  [Nasazení nového klienta elektronického obchodu](deploy-ecommerce-site.md)

  [Nastavení kanálu online obchodu](online-stores.md)

  [Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

  [Přidružení webu Dynamics 365 Commerce k online kanálu](associate-site-online-store.md)

  [Správa souborů robots.txt](manage-robots-txt-files.md)

  [Hromadné odeslání přesměrování URL adresy](upload-bulk-redirects.md)

  [Nastavení klienta B2C v Commerce](set-up-B2C-tenant.md)

  [Nastavení vlastních stránek pro přihlášení uživatelů](custom-pages-user-logins.md)

  [Konfigurace několika klientů B2C v prostředí Commerce](configure-multi-B2C-tenants.md)

  [Přidání podpory pro síť CDN](add-cdn-support.md)

  [Povolení zjišťování obchodu na základě polohy](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]