---
title: Inicializace Commerce Scale Unit (cloud)
description: Toto téma vysvětluje, jak inicializovat Commerce Scale Unit (cloudovou verzi) v Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.openlocfilehash: 84e70515accde161e7efa36755edec68d26be952
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092206"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Inicializace Commerce Scale Unit (cloud)

[!include[banner](../includes/banner.md)]

Toto téma vysvětluje, jak inicializovat Commerce Scale Unit (cloudovou verzi) v Microsoft Dynamics 365 Commerce.

Pokud používáte sandbox 2. úrovně nebo produkční prostředí, které má verzi aplikace 8.1.2.x nebo novější, musíte inicializovat Commerce Scale Unit (cloudovou verzi), než budete moci používat funkce maloobchodního kanálu buď pro operace pokladního místa (POS). nebo pro operace elektronického obchodování, které využívají Retail Server v cloudu. Inicializace nasadí Commerce Scale Unit (cloudovou verzi).

> [!IMPORTANT]
> U stávajících zákazníků využívajících funkce maloobchodního kanálu v cloudu požadujeme, abyste aktualizovali své maloobchodní kanály na využití Commerce Scale Unit, abychom zajistili nepřetržitou a nepřetržitou podporu pro vaši firmu. Nová prostředí nasazená bez Commerce Scale Unit již nebudou dostávat aktualizace kvality a služeb pro součásti maloobchodního kanálu hostovaného v cloudu. Zákazníci, kteří používají výhradně Commerce Scale Unit (v místním prostředí), nevyžadují žádnou akci. Pokud požadujete rozšíření, kontaktujte svého architekta řešení Microsoft FastTrack.

## <a name="prerequisites"></a>Předpoklady

1. Nasaďte sandbox 2. úrovně nebo produkční prostředí, které má verzi 8.1.2.x nebo novější.
2. V každém prostředí můžete samostatně rozmístit až 2 jednotky Commerce Scale Unit. Pokud požadujete více než 2 jednotky Commerce Scale Unit na prostředí, vytvořte v Microsoft Dynamics Lifecycle Services (LCS), požadavek na podporu, zadejte **Požadavek na další jednotku Commerce Scale Unit** a uveďte ID prostředí, počet jednotek Commerce Scale Unit a požadované oblasti datových center. Požadavek bude splněn do pěti pracovních dnů. Pokud nepožadujete více než 2 jednotky Commerce Scale Unit na prostředí, nemusíte vytvářet požadavek na podporu. 
3. Než budete moci inicializovat Commerce Scale Unit, musíte mít oprávnění vlastníka projektu ve službách Lifecycle Services.
4. Ujistěte se, že jsou ve vašem prostředí povoleny konfigurační klíče maloobchodní licence. Další informace najdete v části [Licenční kódy a sestava konfiguračních klíčů](../sysadmin/license-codes-configuration-keys-report.md) Abyste mohli používat Commerce Scale Unit, musíte mít zapnuté následující klíče.

    - RetailBasic
    - RetaileCommerce – Pokud plánujete používat E-Commerce pro Dynamics 365 Commerce.
    - RetailGiftCard – Pokud plánujete používat dárkové poukazy.
    - RetailInvent – Pokud plánujete používat zásoby.
    - RetailModernPos – Pokud plánujete používat pokladní místo (POS).
    - RetailReplenishment – Pokud plánujete používat doplňování.
    - RetailScheduler
    - RetailStores – pokud plánujete používat pokladní místo.


## <a name="region-availability"></a>Regionální dostupnost
Commerce Scale Unit je k dispozici pro nasazení v následujících regionech.

| Globální umístění | Oblast              | Dostupnost        |
|-----------------|---------------------|---------------------|
| AMERIKA        | Východní USA             | Obecně dostupné |
| AMERIKA        | Východní USA 2           | Obecně dostupné |
| AMERIKA        | Střed USA – sever    | Obecně dostupné |
| AMERIKA        | Střed USA – jih    | Obecně dostupné |
| AMERIKA        | Střed USA          | Obecně dostupné |
| AMERIKA        | USA – západ             | Obecně dostupné |
| AMERIKA        | USA – západ 2           | Obecně dostupné |
| AMERIKA        | Střední Kanada      | Omezená kapacita    |
| AMERIKA        | Kanada – východ         | Omezená kapacita    |
| AMERIKA        | Střed USA – západ     | Omezená kapacita    |
| APAC            | Austrálie – východ      | Obecně dostupné |
| APAC            | Jihovýchodní Asie      | Obecně dostupné |
| APAC            | Japonsko – východ          | Obecně dostupné |
| APAC            | Japonsko – západ          | Obecně dostupné |
| APAC            | Austrálie – jihovýchod | Omezená kapacita    |
| APAC            | Východní Asie           | Omezená kapacita    |
| APAC            | Jižní Indie         | Omezená kapacita    |
| APAC            | Střední Indie       | Omezená kapacita    |
| EMEA            | Evropa – západ         | Obecně dostupné |
| EMEA            | Evropa – sever        | Obecně dostupné |
| EMEA            | Velká Británie – jih            | Omezená kapacita    |
| EMEA            | Velká Británie – západ             | Omezená kapacita    |

Kapacita nasazení v regionech s omezenou kapacitou je extrémně omezená. Požadavky na nasazení jsou vyhodnocovány případ od případu. Máte-li přesvědčivou obchodní potřebu nasazení v oblastech s omezenou kapacitou, odešlete požadavek na podporu s žádostí o přidání do pořadníku.

![Mapa ukazující regionální dostupnost.](media/Commerce-Scale-Unit-Region-Availability.png "Mapa ukazující regionální dostupnost")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Inicializace jednotky Commerce Scale Unit jako součásti nasazení nového prostředí

Ujistěte se, že je k dispozici centrála. To je nutné pro registraci jednotky v centrále během procesu inicializace. Nedoporučuje se inicializovat jednotku, když je centrála ve stavu údržby, protože se může stát, že během procesu údržby nebude dostupná.

1. Ujistěte se, že prostředí centrály je dostupné a není v [režimu údržby](../sysadmin/maintenance-mode.md).
2. V LCS na stránce s podrobnostmi o prostředí vyberte **Vlastnosti prostředí \> Commerce**.
3. Na stránce nasazení Commerce vyberte **Inicializovat**.
4. Vyberte verzi jednotky Commerce Scale Unit, kterou chcete inicializovat.
5. Vyberte oblast pro inicializaci jednotky Commerce Scale Unit.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Konfigurace sítí pro použití Commerce Scale Unit

Po nasazení Commerce Scale Unit se musíte ujistit, že vaše sítě jsou konfigurovány tak, aby pro jednotku využívaly databázi. 

Chcete-li konfigurovat své sítě pro použití databáze Commerce Scale Unit, postupujte takto.

1. V centrále Commerce přejděte na **Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Plánovač obchodu \> Databáze sítě**.
1. V levém podokně vyberte databázi sítě.
1. Na záložce **Maloobchodní síť** vyberte **Přidat** a poté v rozevíracím seznamu vyberte svou maloobchodní síť.
1. Vyberte **Přidat** a poté v rozevíracím seznamu vyberte svou online síť. 

Až budete hotovi, přejděte na **Maloobchod a velkoobchod \> IT pro maloobchod a velkoobchod \> Plán distribuce** a spusťte úlohu 9999.

> [!NOTE] 
> Úloha 9999 synchronizuje všechny nové produkty a zákazníky s jednotkou Commerce Scale Unit. Tento proces může trvat delší dobu. Pokud musí být síť dostupná pouze pro konfiguraci nástroje pro tvorbu webu elektronického obchodu, můžete místo úlohy 9999 spustit úlohu 1070.

### <a name="database-refresh-and-commerce-scale-units"></a>Obnovení databáze a jednotek Commerce Scale Unit

Než začnete, ujistěte se, že jste obeznámeni s [kroky, které je třeba dokončit po aktualizaci databáze u prostředí, která používají funkce Commerce](../database/database-refresh.md).

Záznamy databáze sítí Commerce Scale Unit (ve formuláři Databáze sítě) nelze přesouvat mezi prostředími jako součást aktualizace databáze. Je to proto, že záznamy představují konfiguraci specifickou pro prostředí.

Po obnovení databáze můžete znovu vygenerovat záznam databáze sítě Commerce Scale Unit vydáním příkazu k opětovnému nasazení jednotky Commerce Scale Unit v LCS. Jakákoli operace nasazení nebo údržby v jednotce Commerce Scale Unit se pokusí zaregistrovat jednotku Commerce Scale Unit v centrále, pokud je registrace detekována jako chybějící.

Můžete provést opětovné nasazení jednotky Commerce Scale Unit, aniž byste změnili jakékoli součásti, výběrem nasazení stejné verze, ve které se již vaše jednotka Commerce Scale Unit nachází. To lze provést v LCS pomocí následujících kroků:

1. V LCS na stránce s podrobnostmi o prostředí vyberte **Vlastnosti prostředí \> Maloobchod**.
2. Na stránce nasazení instalace vyberte jednotku Commerce Scale Unit, kterou chcete znovu nasadit.
3. V nabídce ovládání jednotky Commerce Scale Unit vyberte **Aktualizovat**.
4. Na posuvníku vyberte v rozevíracím seznamu **Vybrat verzi** možnost **Určit verzi**.
5. V textovém poli pod polem **Určit verzi** zadejte verzi vaší jednotky Commerce Scale Unit, zobrazenou vedle popisku **Aktuální verze**.
6. Klikněte na tlačítko **Aktualizovat**.

Nemusíte vybírat možnost **Aktualizovat rozšíření**, i když jste rozšíření již dříve použili, protože při aktualizaci jednotky Commerce Scale Unit se automaticky vybere poslední balíček rozšíření aplikovaný na jednotku.

Máte-li více jednotek Commerce Scale Unit, je třeba provést výše uvedenou operaci pro každou jednotku. V případě potřeby můžete tyto operace provádět paralelně.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Nasazení dalších jednotek Commerce Scale Unit (volitelné)

Poté, co inicializujete jednotku Commerce Scale Unit, můžete samostatně nasadit druhou jednotku, pokud vás k tomu vaše licence opravňuje. Chcete-li nasadit více než dvě jednotky Commerce Scale Unit, musíte vytvořit požadavek na podporu. V tomto požadavku uveďte počet jednotek Commerce Scale Unit, které požadujete, název prostředí a požadované oblasti. Další informace o licencování najdete v části [Průvodce licencováním Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Pro každou další jednotku Commerce Scale Unit, kterou nasadíte, doporučujeme vytvořit samostatnou skupinu databáze sítě podle následujících kroků.

1. V centrále Commerce přejděte na **Maloobchodní a velkoobchodní prodej > Retail Headquarters > Nastavení plánovače obchodu > Skupina databáze sítí**.
2. Vytvořit novou skupinu databáze kanálů
3. Pžejděte na **Maloobchodní a velkoobchodní prodej > Retail Headquarters > Nastavení plánovače obchodu > Databáze sítí** a vyberte databázi sítí, která odpovídá nově vytvořené jednotce Commerce Scale Unit.
4. Vyberte **Upravit** a vyberte novou skupinu databáze sítí.
5. Zvolte možnost **Uložit**.
6. Vyberte položku **Spustit úplnou synchronizaci dat** pro vybranou databázi sítí.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Další faktory, které je třeba zvážit při inicializaci součástí sítě Commerce hostované v cloudu ve stávajícím prostředí

Pokud již v prostředí používáte součásti sítě Commerce hostované v cloudu, inicializace jednotky Commerce Scale Unit pomůže zkrátit prostoje při aktualizaci těchto součástí. Před inicializací jednotky Commerce Scale Unit je vyžadováno další plánování.

Když inicializujete svou první jednotku Commerce Scale Unit v prostředí, které používá součásti sítě Commerce hostované v cloudu, proces inicializace migruje vaše sítě spojené se součástmi sítí hostovaných v cloudu do první jednotky. Sítě spojené s jednotkami Commerce Scale Unit nejsou ovlivněny.

Proces migrace je pro sítě transparentní. Po zahájení inicializace jednotky Commerce Scale Unit se automaticky provedou následující operace:

1. Bude vytvořena nová jednotka Commerce Scale Unit, která bude spojena s prostředím.
2. Jednotka Commerce Scale Unit bude registrována jako dostupná databáze sítí v centrále.
3. Všechny sítě mapované na **Výchozí** databázi sítí v centrále bude aktualizována, aby se namapovala na novou jednotku Commerce Scale Unit.
4. Bude provedena úplná synchronizace dat Commerce Data Exchange (CDX), aby byla data sítě přenesena do nové jednotky Commerce Scale Unit.

**Plánování a testování inicializace jednotky Commerce Scale Unit** Obecným pravidlem je, že při inicializaci jednotky Commerce Scale Unit musíte naplánovat pětihodinové období odstávky pro operace obchodu a také jakékoli operace sítí elektronického obchodu, které využívají Retail Server nebo cloudové pokladní místo.

1. Proveďte aktualizaci databáze z produkčního prostředí do prostředí UAT sandboxu. 
2. Inicializujte jednotku Commerce Scale Unit v prostředí UAT sandboxu. 
3. Poznamenejte si čas dokončení inicializace jednotky Commerce Scale Unit. Ten můžete srovnat s dobou, kterou tato operace zabere ve vašem produkčním prostředí, během kterého nebudou dostupné operace obchodu a elektronického obchodu.

Před inicializací jednotky Commerce Scale Unit musíte provést následující dodatečné kroky.

- **Uzavřete všechny směny pokladního místa** – Po migraci nebudou uživatelé POS schopni uzavřít žádné směny, které byly aktivní během procesu migrace.
- **Ověřte, že byly úspěšně dokončeny všechny úlohy na vyžádání** – Doporučuje se, aby úlohy na vyžádání pro synchronizaci čekajících transakcí byly dokončeny před inicializací CSU.
- **Odhlaste se ze všech POS zařízení** -–Operace POS nejsou během migrace podporovány.
- **Odvolejte a zrušte všechny pozastavené transakce v POS** – Pozastavené transakce nejsou v rámci inicializace zachovány.

> [!IMPORTANT]
> V rámci inicializace jednotky Commerce Scale Unit budou předchozí pozastavené transakce ztraceny a nelze je odvolat. 

Během období inicializace se projeví tyto změny:

- Sítě Commerce hostované v cloudu nebudou fungovat, dokud nezapnete offline režim POS.
- Zařízení POS se zapnutým režimem offline budou mít omezenou funkčnost.
- Všichni klienti elektronického obchodu, kteří jsou závislí na Retail Serveru, budou přerušeni.
- Sítě, které jsou hostovány na jednotkách Commerce Scale Unit (v místním prostředí), nebudou ovlivněny.
- Funkčnost centrály není ovlivněna.

Po dokončení inicializace se stane následující:

- Stav aktivace zařízení všech aktivovaných zařízení POS je zachován, což znamená, že zařízení nebude nutné znovu aktivovat.
- Samostatné instance hardwarových stanic budou nadále fungovat.
- Zprávy na straně kanálu POS budou resetovány a nebudou zobrazovat data z doby před inicializací.
- Operace Zobrazit deník bude také resetována a nezobrazí data z doby před inicializací.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
