---
title: Dotazování na data pomocí obcházení mobilní aplikace Warehouse Management
description: Tento článek popisuje, jak nakonfigurovat položky nabídky mobilního zařízení s dotazem na data a jak je používat jako součást obcházení.
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 39677ebfb9babeb7246ece4d27ab1813435ca12e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427841"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Dotazování na data pomocí obcházení mobilní aplikace Warehouse Management

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Uvedení funkce

Mobilní aplikace Warehouse Management poskytuje možnost skenování čárových kódů a poskytuje snadný a přesný způsob, jak zachytit data jako součást vašich skladových procesů. Čárové kódy se však někdy poškodí a stanou se nečitelnými nebo požadované datové informace nemusí existovat jako čárový kód v tocích vašich obchodních procesů. V těchto případech může ruční zadávání dat trvat dlouho a může dokonce způsobit zachycení nesprávných dat. Výsledkem může být snížená efektivita a nižší úroveň služeb.

Pomocí flexibilního procesu dotazování na data mohou pracovníci snadno vyhledat požadované informace v rámci vestavěných toků mobilních aplikací Warehouse Management a použít možnosti filtrování tak, aby se zobrazila pouze relevantní data. Ruční výběr je proto rychlejší a přesnější.

Například v toku příjmu nákupní objednávky je číslo nákupní objednávky vyžadováno, aby odpovídalo příchozím zásobám. V rámci tohoto procesu můžete snadno nakonfigurovat položky nabídky tak, aby poskytovaly zobrazení seznamu karet s příslušnými čísly nákupních objednávek. Tímto způsobem můžete pokračovat v toku příjmu pomocí rychlého přístupu typu výběr namířením. Tento článek poskytuje příklady scénářů, ale funkce lze také použít v rámci libovolného nebo všech vašich toků mobilních aplikací Warehouse Management.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Zapnutí funkce toku datového dotazu a její předpoklady

Než budete moci používat funkce popsané v tomto článku, musíte provést následující postup a zapnout požadované funkce.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**. (Další informace o tom, jak používat pracovní prostor **Správa funkcí**, naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Pokud používáte Supply Chain Management verze 10.0.28 nebo starší, zapněte funkci v seznamu následujícím způsobem:

    - **Modul:** *Řízení skladu*
    - **Název funkce:** *pokyny ke krokům aplikace Warehouse*

    Tato funkce je předpokladem pro funkci *Tok dotazu na data aplikace Warehouse Management*. Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout. Pro více informací o funkci *Pokyny pro krok aplikace Warehouse* viz [Přizpůsobení názvů kroků a pokynů pro mobilní aplikaci Warehouse Management](mobile-app-titles-instructions.md).

1. Zapněte funkci, která je zde uvedena, následujícím způsobem:

    - **Modul:** *Řízení skladu*
    - **Název funkce:** *Obcházení aplikace Warehouse Management*

    Tato funkce je předpokladem pro funkci *Tok dotazu na data aplikace Warehouse Management*. Od verze Supply Chain Management 10.0.29 je ve výchozím nastavení zapnuta. Pro více informací o funkci *Obcházení aplikace Warehouse Management*, viz [Konfigurace objížděk pro kroky v položkách nabídky mobilního zařízení](warehouse-app-detours.md).

1. Pokud funkce *Obcházení aplikace Warehouse Management* ještě nebyla zapnuta, aktualizujte názvy polí v mobilní aplikaci Warehouse Management tím, že přejdete na **Warehouse Management \> Nastavení \> Mobilní zařízení \> Názvy polí aplikace Warehouse** a vyberete **Vytvořit výchozí nastavení**. Opakujte tento krok pro každou právnickou osobu (společnost), kde používáte mobilní aplikaci Warehouse Management. Další informace viz [Konfigurace polí pro mobilní aplikaci Řízení skladu](configure-app-field-names-priorities-warehouse.md).
1. Zapněte funkci, která je zde uvedena, následujícím způsobem:

    - **Modul:** *Řízení skladu*
    - **Název funkce:** *Tok zjištění dat aplikace Warehouse Management*

    Tato funkce je funkce popsaná v tomto článku.

## <a name="example-scenarios"></a>Ukázkové scénáře

Tento článek používá příklady scénářů, které ukazují, jak můžete použít funkci *Tok dotazů na data aplikace Warehouse Management* pro zlepšení toku potvrzení o nákupu. Scénáře používají standardní ukázková data, která zahrnují tok s názvem *Příjem nákupu*. Tento tok začíná výzvou pracovníkům, aby určili číslo nákupní objednávky, které obdrží. Abyste pracovníkům pomohli snadněji identifikovat nákupní objednávku, vylepšíte první stránku toku přidáním následujících nových možností dotazu jako [obcházení](warehouse-app-detours.md):

- **Vyhledat nákupní objednávky podle dodavatele** – Otevřete stránku, která vyzve pracovníky k zadání jména dodavatele nebo části jména dodavatele. Je možné použít zástupné znaky. Například, pokud pracovník dnes očekává příchozí dodávku od dodavatele, který zahrnuje *Vývrtka* v názvu, může zadat **Vývr\*** pro zobrazení sady karet pro otevřené objednávky, které obsahují tento text. Každá karta má několik polí, která poskytují informace o každé nákupní objednávce. Kromě jména dodavatele můžete karty navrhnout tak, aby zobrazovaly číslo účtu dodavatele, datum dodání a stav dokladu.
- **Vyhledat dnešní nákupní objednávky** – Otevřete stránku, která nevyzývá pracovníky k zadání dat, ale místo toho zobrazuje předem nakonfigurované filtry (jako je dnešní datum). Na stránce se pak zobrazí sada karet, které odpovídají filtru. Pracovníci postupují tak, že pro nákupní objednávku vyberou kartu, na kterou chtějí evidovat položky zásob.
- **Vyhledání nákupní objednávky podle položky** – Otevřete stránku, která vyzve pracovníky, aby naskenovali čárový kód jakékoli položky v doručených zásobách. Tok pak vypíše všechny otevřené nákupní objednávky, které obsahují řádky pro naskenované číslo položky. Chcete-li pokrýt situace, kdy čárový kód nelze přečíst, můžete na tuto stránku přidat další vyhledávání obcházení, které umožní pracovníkům hledat čísla položek v rámci konkrétní nákupní objednávky.

V každém případě pracovník identifikuje nákupní objednávku výběrem karty a poté se vrátí na první stránku, která zobrazuje vybrané číslo nákupní objednávky. Pracovník pak může pokračovat v toku registrace skladové položky.

## <a name="enable-sample-data"></a>Povolit ukázková data

Chcete-li pracovat s příklady scénářů popsanými v tomto článku, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu *USMF* (společnost).

## <a name="configure-the-mobile-device-menu-items"></a>Konfigurace položek nabídky mobilního zařízení

Chcete-li vytvořit každou z nových možností dotazu, které musíte přidat na první stránku toku, musíte ji nastavit jako položku nabídky mobilního zařízení. Později zpřístupníte možnosti dotazu jako obcházení toku *Příjem nákupu*.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>Vytvoření položky nabídky „Vyhledat nákupní objednávky podle dodavatele“

Vytvořte položku nabídky **Vyhledat nákupní objednávky podle dodavatele** podle následujících kroků.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně Akce vyberte možnost **Nová**, abyste přidali novou položku mobilního zařízení.
1. Pro novou položku nabídky nastavte následující hodnoty:

    - **Název položky nabídky:** *Vyhledat nákupní objednávky podle dodavatele*
    - **Název:** *Vyhledat nákupní objednávky podle dodavatele*
    - **Režim:** *Nepřímý*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Kód aktivity:** *Dotaz na data*
    - **Použít průvodce procesem:** *Ano* (Tato hodnota je vybrána automaticky.)
    - **Název tabulky:** *PurchTable* (Chcete vyhledat čísla nákupních objednávek z této tabulky.)

1. V podokně akcí vyberte **Upravit dotaz** k definování dotazu, který je založen na vybrané základní tabulce (v tomto případě na tabulce nákupních objednávek).
1. V dialogovém okně Editor dotazů na kartě **Rozsah** přidejte do mřížky následující řádky.

    | Tabulka | Odvozená tabulka | Pole | Kritéria |
    |---|---|---|---|
    | Nákupní objednávky | Nákupní objednávky | Stav nákupní objednávky | Otevřená objednávka |
    | Nákupní objednávky | Nákupní objednávky | Datum dodání | (dayRange(-10,10)) |
    | Nákupní objednávky | Nákupní objednávky | Jméno dodavatele | |

1. Vyberte **OK**.

    V tomto příkladu je nová položka nabídky nakonfigurována tak, aby nacházela otevřené nákupní objednávky, u kterých se očekává, že dorazí kdykoli mezi 10 dny v minulosti a 10 dny v budoucnu.

    V dotazu byl sloupec **Kritéria** pro *Jméno prodejce* ponechán prázdný. Pracovníci tedy budou moci zadat tuto hodnotu, když budou používat mobilní aplikaci Warehouse Management.

    Pokud chcete určit, jak bude seznam řazen, můžete nastavit řazení na kartě **Řazení**.

1. Kromě definování dotazu musíte vybrat, která pole se budou zobrazovat na kartách na stránce seznamu dotazů. V podokně akcí proto vyberte možnost **Seznam polí**.
1. Na stránce **Seznam polí** nastavte následující hodnoty:

    - **Pole zobrazení 1:** *PurchId* (Toto pole se zobrazí jako záhlaví každé karty.)
    - **Pole zobrazení 2:** *PurchStatus*
    - **Pole zobrazení 3:** *PurchName*
    - **Pole zobrazení 4:** *OrderAccount*
    - **Pole zobrazení 5:** *DeliveryDate*
    - **Pole zobrazení 6:** *displayDocumentStatus()* (Tato hodnota je metoda zobrazení, jak naznačuje „()“ na konci.)

1. V podokně akcí vyberte **Uložit**. Poté stránku zavřete.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>Vytvoření položky nabídky „Vyhledat nákupní objednávky pro dnešek“

Vytvořte položku nabídky **Vyhledat nákupní objednávky pro dnešek** podle následujících kroků.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně Akce vyberte možnost **Nová**, abyste přidali novou položku mobilního zařízení.
1. Nastavte následující hodnoty pro novou položku:

    - **Název položky nabídky:** *Vyhledat nákupní objednávky pro dnešek*
    - **Název:** *Vyhledat nákupní objednávky pro dnešek*
    - **Režim:** *Nepřímý*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Kód aktivity:** *Dotaz na data*
    - **Použít průvodce procesem:** *Ano* (Tato hodnota je vybrána automaticky.)
    - **Název tabulky:** *PurchTable* (Chcete vyhledat čísla nákupních objednávek z této tabulky.)

1. V podokně akcí vyberte **Upravit dotaz** k definování dotazu, který je založen na vybrané základní tabulce (v tomto případě na tabulce nákupních objednávek).
1. V dialogovém okně Editor dotazů na kartě **Rozsah** přidejte do mřížky následující řádky.

    | Tabulka | Odvozená tabulka | Pole | Kritéria |
    |---|---|---|---|
    | Nákupní objednávka | Nákupní objednávka | Stav nákupní objednávky | Otevřená objednávka |
    | Nákupní objednávka | Nákupní objednávka | Datum dodání | (Day(0)) |

1. Vyberte **OK**.

    V tomto příkladu je nová položka nabídky nakonfigurována tak, aby nacházela otevřené nákupní objednávky, které mají být doručeny dnes.

    Pokud chcete určit, jak bude seznam řazen, můžete nastavit řazení na kartě **Řazení**.

1. Kromě definování dotazu musíte vybrat, která pole se budou zobrazovat na kartách na stránce seznamu dotazů. V podokně akcí proto vyberte možnost **Seznam polí**.
1. Na stránce **Seznam polí** nastavte následující hodnoty:

    - **Pole zobrazení 1:** *PurchName* (Toto pole se zobrazí jako záhlaví každé karty.)
    - **Pole zobrazení 2:** *PurchId*
    - **Pole zobrazení 3:** *PurchStatus*
    - **Pole zobrazení 4:** *DlvMode*
    - **Pole zobrazení 5:** *DlvTerm*
    - **Pole zobrazení 6:** *OrderAccount*
    - **Pole zobrazení 7:** *VendorName()* (Tato hodnota je metoda zobrazení, jak naznačuje „()“ na konci.)

1. V podokně akcí vyberte **Uložit**. Poté stránku zavřete.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>Vytvoření položky nabídky „Vyhledat nákupní objednávky podle položky“

Vytvořte položku nabídky **Vyhledat nákupní objednávky podle položky** podle následujících kroků.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně Akce vyberte možnost **Nová**, abyste přidali novou položku mobilního zařízení.
1. Nastavte následující hodnoty pro novou položku:

    - **Název položky nabídky:** *Vyhledat nákupní objednávky podle položky*
    - **Název:** *Vyhledat nákupní objednávky podle položky*
    - **Režim:** *Nepřímý*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Kód aktivity:** *Dotaz na data*
    - **Použít průvodce procesem:** *Ano* (Tato hodnota je vybrána automaticky.)
    - **Název tabulky:** *PurchLine* (Chcete vyhledat čísla nákupních objednávek na základě čísla položky prostřednictvím dat řádku.)

1. V podokně akcí vyberte **Upravit dotaz** k definování dotazu, který je založen na vybrané základní tabulce (v tomto případě na tabulce řádků nákupní objednávky, ale můžete použít kteroukoli z hodnot, které souvisí se záhlavím, a to spojením s *PurchTable*).
1. V dialogovém okně Editor dotazů na kartě **Rozsah** přidejte do mřížky následující řádky.

    | Tabulka | Odvozená tabulka | Pole | Kritéria |
    |---|---|---|---|
    | Řádky nákupní objednávky | Řádky nákupní objednávky | Stav řádku | Otevřená objednávka |
    | Řádky nákupní objednávky | Řádky nákupní objednávky | Datum dodání | (dayRange(-10,10)) |
    | Řádky nákupní objednávky | Řádky nákupní objednávky | Číslo položky | |

1. Vyberte **OK**.

    V tomto příkladu je nová položka nabídky nakonfigurována tak, aby nacházela otevřené řádky nákupní objednávky, u kterých se očekává, že dorazí kdykoli mezi 10 dny v minulosti a 10 dny v budoucnu.

    V dotazu byl sloupec **Kritéria** pro *Číslo položky* ponechán prázdný. Pracovníci tedy budou moci zadat tuto hodnotu, když budou používat mobilní aplikaci Warehouse Management.

    Pokud chcete určit, jak bude seznam řazen, můžete nastavit řazení na kartě **Řazení**.

1. Kromě definování dotazu musíte vybrat, která pole se budou zobrazovat na kartách na stránce seznamu dotazů. V podokně akcí proto vyberte možnost **Seznam polí**.
1. Na stránce **Seznam polí** nastavte následující hodnoty:

    - **Pole zobrazení 1:** *PurchId* (Tato hodnota pole bude použita jako záhlaví každé karty.)
    - **Pole zobrazení 2:** *VendAccount*
    - **Pole zobrazení 3:** *PurchQty*
    - **Pole zobrazení 4:** *PurchUnit*
    - **Pole zobrazení 5:** *PurchStatus*

1. V podokně akcí vyberte **Uložit**. Poté stránku zavřete.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Přidání nových položek nabídky mobilního zařízení do nabídky

Vaše tři nové položky nabídky mobilního zařízení jsou nyní připraveny k přidání do nabídky mobilního zařízení. Tento úkol musí být proveden, než lze položky nabídky použít jako součást procesu obcházení. V tomto příkladu vytvoříte novou podnabídku a přidáte do ní nové položky nabídky.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. V podokně akcí zvolte **Nový**.
1. Nastavte následující hodnoty v záhlaví nového záznamu:

    - **Název:** *Zeptat se*
    - **Popis:** *Zeptat se*

1. V seznamu **Dostupné nabídky a položky nabídky** vyberte první položku nabídky mobilního zařízení, kterou jste právě vytvořili. Poté stisknutím tlačítka se šipkou doprava přesuňte tuto položku nabídky do seznamu **Struktura nabídky**.
1. Opakujte předchozí krok pro další dvě nové položky nabídky.
1. V podokně seznamu vlevo vyberte nabídku **Hlavní**.
1. V seznamu **Dostupné nabídky a položky nabídky** přejděte dolů na **Nabídky** a vyberte novou nabídku **Zeptat se**. Poté stisknutím tlačítka se šipkou doprava přesuňte tuto položku nabídky do seznamu **Struktura nabídky**.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Konfigurace obcházení pro kroky mobilního zařízení

Pro provedení nastavení musíte nyní použít konfiguraci obcházení na stránce **Kroky mobilního zařízení** k přidání tří nových položek nabídky mobilního zařízení do stávajícího kroku identifikace nákupní objednávky v toku *Příjem nákupu*.

1. Přejděte do **Řízení skladu \> Nastavení > Mobilní zařízení \> Kroky mobilního zařízení**.
1. Do pole **Filtr** zadejte *PONum*. Poté vyberte z rozevíracího seznamu *ID kroku: "PONum"*.
1. Zatímco je nalezený záznam vybrán v mřížce, vyberte **Přidat konfiguraci kroku** na podokně akcí. V rozevíracím dialogovém okně, které se zobrazí nastavte pole **Položka nabídky** na *Příjem nákupu*. Poté zvolte **OK** a zavřete dialogové okno.
1. Na stránce údajů pro konfiguraci nového kroku (**Příjem nákupu: PONum**) na pevné záložce **Dostupná obcházení (položky nabídky)** vyberte **Přidat** na panelu nástrojů.
1. V dialogovém okně **Přidat obcházení** vyhledejte a vyberte položku nabídky **Vyhledat nákupní objednávky podle dodavatele**, kterou jste dříve vytvořili.
1. Vyberte **OK** k zavření dialogového okna a přidání vybrané položky nabídky do seznamu obcházení.
1. Vyberte nové obcházení a poté na panelu nástrojů vyberte **Vybrat pole k odeslání**.
1. V dialogovém okně **Vybrat pole k odeslání** nic nepřidávejte do části **Odeslat z příjmu nákupu**, protože do položky nabídky obcházení nechcete předávat žádné hodnoty. Nicméně v části **Načíst z nákupní objednávky z vyhledávání podle dodavatele** nastavte následující hodnotu pro prázdný řádek, který tam již byl přidán:

    - **Kopírovat z nákupního objednávek z vyhledávání podle dodavatele:** *Nákupní objednávka*
    - **Vložit do příjmu nákupu:** *Nákupní objednávka*

1. Zvolte **OK** a zavřete dialogové okno.
1. Opakujte kroky 4 až 9 pro další dvě nové položky nabídky (**Vyhledat nákupní objednávky pro dnešek** a **Vyhledat nákupní objednávky podle položky**). Pokud jde o položku nabídky **Vyhledat objednávky podle dodavatele**, nechcete do těchto obcházení posílat žádná data, ale chcete vrátit číslo objednávky.
1. Zavřete stránku.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Vyzkoušejte tok příjmu nákupu, který má jako součást obcházení dotaz na data

Chcete-li otestovat nastavení nové mobilní aplikace, postupujte podle těchto kroků.

1. Vytvořte několik nákupních objednávek, které mají řádky pro sklad 51.
1. Přejděte na mobilní zařízení nebo emulátor, ve kterém je spuštěná mobilní aplikace Řízení skladu, a přihlaste se do skladu 51 pomocí *51* jako ID uživatele a *1* jako heslo.
1. V nabídce mobilní aplikace vyberte **Příchozí** a pak **Příjem nákupu**.

    Měli byste vidět následující stránku, která obsahuje tři nové položky nabídky.

    ![Příjem nákupu pomocí čísla nákupní objednávky.](media/wma-purchase-receive-po-num-with-detours.png "Příjem nákupu pomocí čísla nákupní objednávky")

1. Vyzkoušejte různé možnosti a všimněte si, že můžete poslat zpět číslo nákupní objednávky výběrem jedné z karet v seznamu.

    ![Příjem nákupu pomocí vyhledávání nákupní objednávky podle dodavatele, příklad 1.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Příjem nákupu pomocí vyhledávání nákupní objednávky podle dodavatele, příklad 1")

    ![Příjem nákupu pomocí vyhledávání nákupní objednávky podle dodavatele, příklad 2.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Příjem nákupu pomocí vyhledávání nákupní objednávky podle dodavatele, příklad 2")

> [!TIP]
> Namísto spuštění přijímacího toku vyhledáváním z položky nabídky **Příjem nákupu** můžete začít z toku dotazů (**Hlavní \> Dotázat se \> Vyhledat nákupní objednávky podle dodavatele**) a vyvolat obcházení pro spuštění požadovaného toku výběrem jedné z karet v seznamu. Chcete-li použít tento přístup, můžete definovat obcházení na stránce **Kroky pro mobilní zařízení** pro krok, který má hodnotu **ID kroku** *GenericDataInquiryList*. Za předpokladu, že je funkce [*Víceúrovňové obcházení pro mobilní aplikaci Warehouse Management*](warehouse-app-detours.md) pro váš systém zapnutá, v případě potřeby můžete také přidat další obcházení (tato funkce přidává podporu až dvou úrovní obcházení a lze ji přizpůsobit tak, aby podporovala další úrovně).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
