---
title: Zpracování přepravovaného zboží
description: Toto téma popisuje, jak pracovat s objednávkami přepravovaného zboží. Když je objednávka nebo cesta nastavena tak, aby používala zpracování přepravovaného zboží, může být zboží fakturováno před jeho přijetím do skladu ke spotřebě.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: fff3c3cfe5d0628fd4df6e719b72bc134c9d9c0a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909444"
---
# <a name="goods-in-transit-processing"></a>Zpracování přepravovaného zboží

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak pracovat s objednávkami přepravovaného zboží. Tento typ objednávky se používá pouze v modulu **Náklady za doručení**. Když je objednávka nebo cesta nastavena tak, aby používala zpracování přepravovaného zboží, nemusíte čekat na přijetí zboží do skladu, než může být zboží fakturováno. Místo toho je zboží fakturováno, když opouští výchozí sklad nebo přístav dodavatele, a finanční náklady jsou uznány při zahájení cesty. Tato funkce vám umožní správně převzít vlastnictví zásob, protože zboží se často stává majetkem vaší organizace, když opustí přepravní přístav.

Při použití objednávek přepravovaného zboží jsou finančně aktualizované položky přijímány v prozatímním skladu, který se nazývá tranzitní sklad zboží. Zboží poté zůstane v tomto skladu, dokud ho nebude možné přijmout v konečném cílovém skladu (tj. ve skladu, který je definován na nákupním řádku). Nelze ho ručně odstranit.

Dokud jsou položky na cestě, nejsou k dispozici v zásobách a nelze je ze zásob vybrat k dodání. Můžete si však prohlédnout inventář přepravovaného zboží. Zboží používáte také pro hlavní plánování. V takovém případě použijte potvrzené datum dodání na řádku nákupní objednávky jako očekávané datum, kdy budou zásoby dostupné ke spotřebě.

Následující části popisují nastavení, které je nutné ke zpracování zásob a cest pomocí konceptu a funkčnosti přepravovaného zboží.

## <a name="terms-of-delivery"></a>Dodací podmínky

Když povolíte modul **Náklady za doručení**, standardní entita *dodací podmínky* je vylepšena o podporu funkce přepravovaného zboží.

Když je možnost **Správa přepravovaného zboží** je nastavena na *Ano* pro příslušné záznamy dodacích podmínek, je zboží umístěno do tranzitního skladu zboží. Tato akce se aktivuje pouze v případě, že před zpracováním faktury nebude zpracován příjem zásob. Když mají dodací podmínky objednávky nastaveno použití přepravovaného zboží, uživatelé již nemohou zaúčtovat příjemku produktu pro objednávku. Pokud se o to pokusí, dojde k chybě. Chybová zpráva uvádí, že k pokračování je nutné použít funkci přepravovaného zboží.

Chcete-li pracovat s informacemi o dodacích podmínkách pro přepravované zboží, přejděte na uzel **Zásobování a zdroje \> Nastavení \> Rozdělení \> Dodací podmínky**. Následující tabulka popisuje pole, která modul **Náklady za doručení** přidává do stránky **Dodací podmínky** za účelem podpory funkce přepravovaného zboží. Obě pole jsou na záložce **Obecné**. Další informace o dalších polích na této stránce najdete v tématu [Dodací podmínky (formulář)](/dynamicsax-2012//terms-of-delivery-form).

| Pole | popis |
|---|---|
| Výchozí přístav je povinný | Tuto možnost nastavte na *Ano* pokud je přepravní přístav povinný tam, kde platí dodací podmínky.. |
| Správa přepravovaného zboží | Tuto možnost nastavte na *Ano*, chcete-li použít správu přepravovaného zboží tam, kde platí dodací podmínky. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Sklady pro přepravované zboží a nedostatečné dodávky

Když povolíte modul **Náklady za doručení**, je standardní entita *sklady* vylepšena, aby bylo možné fakturovat nákupní objednávky v době, kdy je zboží v tranzitním skladu.

Náklady za doručení přidávají dva nové typy skladu: *přepravované zboží* a *nedostatečná dodávka*. Sklady obou typů lze vybrat jako výchozí sklady. Úspěšné zpracování objednávek přepravovaného zboží vyžaduje, aby tranzitní sklad zboží i sklad pro nedostatečné dodávky byly konfigurovány na stránce **Sklady**. Potom u každého výchozího skladu, který bude použit v modulu Náklady za doručení a s přepravovaným zbožím, musí být pro dostupné sklady každého typu vybrán tranzitní sklad zboží a sklad pro nedostatečné dodávky.

Typ skladu pro *přepravované zboží* bude přidružen k vašemu tranzitnímu skladu zboží a tento sklad bude použit ke zpracování zboží na objednávkách přepravovaného zboží před jeho přijetím v konečném cílovém skladu. Obecně platí, že pro každé místo postačuje jeden tranzitní sklad zboží, pokud jsou místo a sklad jediné dimenze zásob, které se používají pro správu zásob. Pokud se také používá dimenze Umístění zásob, musí být pro každou kombinaci místa a skladu nastaven tranzitní sklad zboží, aby bylo možné určit také výchozí umístění.

Chcete-li pracovat s nastavením přepravovaného zboží pro vaše sklady, přejděte na uzel **Řízení zásob \> Nastavení \> Rozdělení zásob \> Sklady**. Následující tabulka popisuje pole, která modul **Náklady za doručení** přidává do stránky **Sklady** za účelem podpory funkce přepravovaného zboží. Obě pole se zobrazí na záložce **Obecné**. Chcete-li získat informace o ostatních polích na stránce, přečtěte si téma [Sklady (formulář)](/dynamicsax-2012//warehouses-form).

| Pole | popis |
|---|---|
| Sklad přepravovaného zboží | Určete tranzitní sklad zboží, který souvisí s hlavním skladem. |
| Sklad nedostatečného dodání | Určete sklad pro nedostatečné dodávky, který souvisí s hlavním skladem. |

## <a name="posting-rules-for-landed-cost"></a>Pravidla zaúčtování nákladů za doručení

Modul Náklady za doručení přidává dvě nová pravidla účtování, která můžete konfigurovat. Tato pravidla účtování se používají k finančnímu zaúčtování přímých částek faktury za nákupní objednávku k identifikaci vlastnictví zboží, když opouští místo původu. Tento proces nahrazuje koncept *přijaté zboží, které nebylo dosud fakturováno*, protože zboží je fakturováno před jeho přijetím. <!-- KFM: Add a link to the related scenario when available. -->

Chcete-li pracovat s profily účtování, přejděte na uzel **Řízení zásob \> Nastavení \> Zaúčtování \> Zaúčtování**. Na kartě **Nákupní objednávka** jsou k dispozici následující nová pravidla účtování:

- **Náklady za doručení, přepravované zboží** - Určete pravidla účtování pro správu přepravovaného zboží.
- **Náklady za doručení, časové rozlišení nákladů** – Určete pravidla účtování pro časové rozlišení nákladů.

## <a name="goods-in-transit-orders"></a>Objednávky přepravovaného zboží

Objednávky přepravovaného zboží můžete kontrolovat a spravovat přímo v modulu **Náklady za doručení**. Objednávky přepravovaného zboží můžete zpracovávat přímo ve stránce **Objednávky přepravovaného zboží**. Případně můžete přejít na cestu, která je asociována s objednávkami přepravovaného zboží, a zpracovat celou cestu, přepravní kontejner nebo folio. Když fakturujete cestu a vytvoříte objednávky přepravovaného zboží, vytvoří se nová objednávka přepravovaného zboží pro každou kombinaci zásob a dimenzí zásob, která je přidružena k řádku nákupní objednávky.

Pro správu přepravovaného zboží používá modul Náklady za doručení dvoustupňový postup:

1. Zboží je přijato, když je zpracována skladová faktura a je jí přiřazen stav *Na cestě*.
1. Objednávka přepravovaného zboží je zpracována na stránce **Objednávky přepravovaného zboží** a poté přijata do skladu, který je uveden v nákupní objednávce. V tomto okamžiku se stav změní na *Přijato*.

Chcete-li pracovat s objednávkami přepravovaného zboží, přejděte na **Náklady za doručení \> Periodické úkoly \> Objednávky přepravovaného zboží**.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Příjem zásob z tranzitního skladu zboží

Zboží z objednávky přepravovaného zboží můžete přijímat mnoha způsoby, v závislosti na nastavení vašeho systému.

### <a name="in-transit-receiving"></a>Příjem během přepravy

Příjem během přepravy je možné provést na kterékoli z následujících stránek:

- Na stránce **Objednávky přepravovaného zboží** vyberte řádek a poté v podokně akcí vyberte příkaz **Přijmout**.
- Na stránce **Všechny cesty** vyberte nebo otevřete cestu. Poté v podokně akcí na kartě **Spravovat** vyberte ve skupině **Přepravované zboží** příkaz **Přijmout přepravované zboží**.
- Na stránce **Všechny přepravní kontejnery** vyberte nebo otevřete přepravní kontejner. Poté v podokně akcí na kartě **Spravovat** vyberte ve skupině **Přepravované zboží** příkaz **Přijmout přepravované zboží**.
- Na stránce **Všechna folia** vyberte nebo otevřete folio. Poté v podokně akcí na kartě **Spravovat** vyberte ve skupině **Přepravované zboží** příkaz **Přijmout přepravované zboží**.

> [!NOTE]
> Příjem během přepravy se obecně používá v situacích, kdy se nepoužívají umístění a sledování dávky/série.

### <a name="arrival-journal"></a>Deník doručení

Zboží můžete také přijímat vytvořením deníku doručení. Deník doručení můžete vytvořit přímo ve stránce cesty. Zda se deník doručení používá k příjmu zboží, určují osvědčené postupy, které vaše organizace zavedla.

1. Otevřete cestu, kontejner nebo folio.
1. V podokně akcí na kartě **Spravovat** ve skupině **Funkce** vyberte **Vytvořit deník doručení**.
1. V dialogovém okně **Vytvoření deníku doručení** nastavte následující hodnoty:
    - **Inicializovat množství** – Nastavte tuto možnost na *Ano*, když má být množství nastaveno z množství v přepravě. Pokud je tato možnost nastavena na *Ne*, není z řádků přepravovaného zboží nastaveno žádné výchozí množství.
    - **Vytvořit z přepravovaného zboží** – Nastavte tuto možnost na *Ano*, chcete-li přebírat množství z vybraných řádků v tranzitu pro vybranou cestu, kontejner nebo folio.
    - **Vytvořit z řádků objednávky** – Nastavte tuto možnost na *Ano*, chcete-li nastavit výchozí množství v deníku doručení z řádků nákupní objednávky. Tímto způsobem lze nastavit výchozí množství v deníku doručení pouze v případě, že množství na řádku nákupní objednávky odpovídá množství na objednávce přepravovaného zboží.

1. Zpracujte deník doručení podle popisu v tématu [Registrace příjmu zboží pomocí deníku doručení zboží](/dynamicsax-2012/appuser-itpro/register-item-receipts-with-an-item-arrival-journal).

> [!NOTE]
> Deník doručení se obecně používá v situacích, kdy se používají umístění a sledování dávky/série, ale nepoužívá se řízení skladu.
>
> Výchozí umístění příjmu by nemělo být uvedeno na řádcích objednávky, pokud bude v deníku doručení uvedeno místo vyskladnění.

## <a name="warehouse-management"></a>Řízení skladu

Když povolíte modul **Náklady za doručení**, několik stránek v modulu **Řízení skladu** se upraví tak, aby zpracování objednávek (konkrétně zpracování přepravovaného zboží) bylo možné provádět prostřednictvím modulu **Náklady za doručení**. Tato část popisuje pole a procesy, které jsou přidány do modulu **Řízení skladu**.

### <a name="mobile-device-menu-items"></a>Položky nabídky mobilního zařízení

Zboží lze přijímat pomocí mobilního zařízení, pokud byla nabídka mobilního zařízení a modul **Řízení skladu** nastaveny pro příjem zboží na objednávce přepravovaného zboží. Tato část popisuje nastavení, které je spojeno s příjmem přepravovaného zboží.

Chcete-li nastavit mobilní zařízení pro zpracování přepravovaného zboží, přejděte na uzel **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.

Modul Náklady za doručení přidává do položek nabídky mobilního zařízení následující procesy vytváření prací, které podporují zpracování přepravovaného zboží:

- Příjem položky přepravovaného zboží
- Příjem a vyskladnění položky přepravovaného zboží

Nastavení konfigurace pro tyto procesy se podobá nastavení [procesů vytváření příjmu a vyskladnění nákupních objednávek](/dynamicsax-2012/appuser-itpro/configure-mobile-devices-for-warehouse-work). Proces *Příjem a vyskladnění položky přepravovaného zboží* však také přidá následující pole.

- **Povolit dokončení přepravního kontejneru** – Pokud je tato možnost nastavena na *Ano*, mobilní aplikace Řízení skladu poskytne další možnost s názvem **Přepravní kontejner dokončen**, když je vyskladnění dokončeno. Když je tato možnost vybrána, pracovník bude vyzván k potvrzení, že je kontejner kompletní. V tomto okamžiku budou všechny nedostačující příjmy zpracovány jako transakce nedostatečné dodávky.

### <a name="location-directives"></a>Směrnice skladového místa

Modul Náklady za doručení přidá nový typ pracovního příkazu s názvem *Přepravované zboží* do stránky **Směrnice skladového místa**. Tento typ pracovního příkazu by měl být konfigurován stejným způsobem jako [typy pracovních příkazů nákupní objednávky](/dynamicsax-2012/appuser-itpro/create-a-work-template).

### <a name="work-templates"></a>Šablony práce

Modul Náklady za doručení přidá nový typ pracovního příkazu s názvem *Přepravované zboží* do stránky **Šablony práce**. Tento typ pracovního příkazu by měl být konfigurován stejným způsobem jako [šablony práce nákupní objednávky](/dynamicsax-2012/appuser-itpro/create-a-work-template).