---
title: Zásady konsolidace dodávek
description: Toto téma poskytuje přehled funkcí, které poskytují flexibilní konfiguraci zásad konsolidace dodávek.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationError, WHSShipConsolidationSetShipment, WHSShipConsolidationPolicySelect, WHSShipPlanningListPage, TMSCarrierGroup, WHSShipConsolidationTemplate, WHSShipConsolidationTemplateApply, WHSShipConsolidationTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f895b13b2e11d4cb341f80b3cfeb40ed998ccfc4
ms.sourcegitcommit: d9bffbeae2ba14f06294dd275383077d4d65c4fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654213"
---
# <a name="shipment-consolidation-policies"></a>Zásady konsolidace dodávek

Proces konsolidace dodávek, který používá zásady konsolidace dodávek, umožňuje automatizovanou konsolidaci dodávek během automatizovaného a ručního uvolnění do skladu. Automatizovaná konsolidace, která byla k dispozici před zavedením této funkce, měla pevně zakódovaná pole a byla založena na poli **Konsolidovat dodávku při uvolnění do skladu**, které bylo nastaveno pro sklad.

Zásady konsolidace dodávek se používají pro následující funkce:

- Automatická dávková úloha uvolnění do skladu
- Příkaz **Uvolnit do skladu** v prodejní objednávce nebo převodním příkazu
- Vyhrazená stránka **Uvolnit do skladu**
- Příkaz **Uvolnit do skladu** na stránce **Pracovní plocha plánování nákladu**
- Ruční konsolidace dodávek na stránkách **Konsolidace dodávek** a **Pracovní plocha konsolidace dodávek**

Před zavedením zásad konsolidace dodávek existovala funkce konsolidace jako nastavení na úrovni skladu. Všechny objednávky pro všechny zákazníky z jednoho skladu byly zpracovány, jako by měly stejné požadavky na konsolidaci. Zásady konsolidace dodávek přidávají podporu pro scénáře, kde různé organizace mají různé požadavky na konsolidaci dodávek.

Dotazy se používají k identifikaci použitelné zásady konsolidace dodávek a poté upravitelná sada polí určuje, jak jsou řádky vytížení seskupeny na úrovni dodávky. (Tento vzorec se podobá vzorci, který následují šablony vln.) Kromě toho byla do každé zásady přidána možnost **Konsolidovat se stávajícími dodávkami**. Když je tato možnost zapnutá, postup *Uvolnění do skladu* nalezne dodávky pro konsolidaci vyhledáním mezi existujícími dodávkami, které byly vytvořeny na základě stejné zásady konsolidace. V tomto případě systém místo vytvoření nové vybere existující dodávku nebo náklad. Systém se však konsoliduje pouze se stávajícími dodávkami, které mají stav *Otevřeno*. Dodávky, které patří do uvolnění vlny se stavem *Uvolněno* nebo vyšší nebudou považovány za cíle pro konsolidace.

Když jsou zpřístupněny zásady konsolidace dodávek, nastavení **Konsolidovat dodávku při uvolnění do skladu**, které bylo dříve k dispozici na stránce natavení **Sklady** je skryté. Pro usnadnění přechodu na novou funkci konsolidace dodávek vytváří funkce na stránce **Zásady konsolidace dodávek** výchozí zásadu, která automaticky zahrnuje staré nastavení pro stávající sklady. Po vytvoření této výchozí zásady nebude nastavení **Konsolidovat dodávku při uvolnění do skladu** na stránce **Sklady** již bráno v úvahu.

Můžete použít stránku **Uvolnění do skladu** pro ruční přepsání použitelné zásady konsolidace stejným způsobem, jakým můžete přepsat zásady plnění.

Můžete použít příkaz **Uvolnění \> Uvolnění do skladu** na stránce **Pracovní plocha plánování vytížení** k sestavení odchozích nákladů, které jsou založeny na řádcích prodejních objednávek a převodních příkazů před provedením uvolnění do skladu. Tato zatížení používají stejnou konsolidační logiku, která byla zavedena společně s konsolidací zásad dodávek.

Můžete použít stránku **Pracovní plocha konsolidace dodávek** pro konsolidaci stávajících dodávek, které ještě nebyly potvrzeny, ale již byly uvolněny do skladu . Tato funkce podporuje scénáře, ve kterých je automatizovaný proces uvolnění, který má vlastní konsolidaci dodávek, spuštěn vícekrát denně, ale potenciální dodatečné konsolidace jsou ručně identifikovány před dokončením dodávky přepravcům během procesu potvrzení. Tato funkce umožňuje konsolidovat odchozí dodávky, které jsou vytvářeny z řádků prodejních objednávek nebo převodních příkazů, kdykoli po odeslání dodávek do skladu, ale před jejich potvrzením.

Stránka **Pracovní plocha konsolidace dodávek** funguje jako pracovní plocha sestavení vytížení, kde můžete posoudit více dodávek současně a přiřadit nekonsolidovanou objednávku ke konkrétní dodávce. Šablony konsolidace dodávek můžete použít k opakovanému posouzení navrhovaných konsolidací a jejich potvrzení. Jsou implementována některá pravidla, která zabraňují neoprávněné konsolidaci a upozorňují vás na možné chyby.

## <a name="overview-of-new-functionality"></a>Přehled nových funkcí

Tato část popisuje stránky, příkazy a funkce, které se změní nebo přidají, když zapnete a použijete funkci *Zásady konsolidace dodávek*.

### <a name="shipment-consolidation-policies-page"></a>Stránka zásad konsolidace dodávek

Zásady jsou rozlišeny podle typu pracovního příkazu. Typ **Prodejní objednávka** představuje dodávky _Prodejní objednávka_ a typ **Převodní příkazy** představují dodávky _Převodní příkazy_.

Každá zásada konsolidace dodávek má dotaz, který definuje, kdy se použije, a pořadové číslo, které určuje pořadí provedení. Konsolidace se použije pro každou jedinečnou kombinaci vybraných polí. Další poskytovaný parametr se používá pro konsolidaci se stávajícími (otevřenými) dodávkami. Zásady se vyhodnocují a používají při každém vytvoření nové dodávky (před zpracováním vln).

Pokud v zásadě chybí povinná pole nebo pokud obsahuje zakázaná pole, je tato zásada označena jako neplatná v části **Vybráno**. Seznamy povinných a zakázaných polí jsou pevně zakódována a lze je rozšířit.

Následující seznam zobrazuje povinná pole. Protože dodávky jsou vždy rozděleny na základě těchto polí, nemůžete seskupit více dodávek, které mají pro tato pole odlišné hodnoty.

- Pro prodejní objednávky:

    - **Číslo účtu:** _WHSShipmentTable.AccountNum_
    - **Příjemce dodávky:** _WHSShipmentTable.DeliveryName_
    - **Poštovní adresa (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Sklad:** _WHSShipmentTable.InventLocationId_

- Pro převodní příkazy:

    - **Ze skladu:** _InventTransferTable.InventLocationIdFrom_
    - **Do skladu:** _InventTransferTable.InventLocationIdTo_

Následující pole nejsou k dispozici pro všechny typy dokumentů. Tato pole nejsou v uživatelském rozhraní viditelná a nelze je použít pro konsolidaci.

- **ID dodávky:** _WHSShipmentTable.ShipmentId_
- **Stav:** _WHSShipmentTable.ShipmentStatus_
- **Zásada konsolidace zásilek:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Typ pracovní transakce:** _WHSShipmentTable.WorkTransType_
- **ID vlny:** _WHSShipmentTable.WaveId_
- **ID nákladu:** _WHSShipmentTable.LoadId_
- **ID dodávky:** _WHSLoadLine.ShipmentId_
- **ID nákladu:** _WHSLoadLine.LoadId_

Ve výchozím nastavení se při vytváření zásady používá jako pole konsolidace sada povinných polí. Seznam však můžete upravit pomocí tlačítek se šipkami doleva a doprava. (Proces se podobá procesu výběru metod v šablonách vln.)

Hodnoty, které uživatelé vyberou pro tato pole, budou použity pro všechny nově vytvořené dodávky, nebo budou přidány k existujícím dodávkám během konsolidace s těmito dodávkami. Pokud dvě dodávky mají stejnou hodnotu pro pole vybrané pro konsolidaci těchto dodávek, dodávky se konsolidují. Stejný princip platí pro všechna následná pole konsolidace, která jsou vybrána. Pokud se hodnoty liší, bude druhá dodávka zahozena a bude vybrána pro novou dodávku. Proces automatizované konsolidace spočívá ve vytvoření všech jedinečných kombinací hodnot pro pole konsolidace dodávek a poté přiřazení dodávky k příslušné kombinaci.

Nevybraná pole jsou během procesu konsolidace ignorována. Pokud dvě dodávky mají různé hodnoty pro nezvolené pole, pole se vymaže (to znamená, že je nastaveno na prázdné). Pokud mají obě dodávky stejnou hodnotu pro nezvolené pole, je pole vyplněno.

Seznam konsolidačních polí (to znamená polí, která budou vymazána, pokud budou mít různé hodnoty) je pevně zakódován. Seznam obsahuje všechna pole, která jsou inicializována z prodejní objednávky nebo řádku převodního příkazu při vytvoření nové dodávky. Jinými slovy, pokud pole není inicializováno z prodejní objednávky nebo z řádku převodního příkazu, bude při přidání nových dat do existující dodávky ignorováno.

### <a name="release-to-warehouse-page"></a>Stránka uvolnění do skladu

- Nové pole ve spodní mřížce ukazuje zásadu konsolidace, která byla použita.
- Nové tlačítko umožňuje ručně vybrat anebo přepsat zásadu konsolidace.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Příkaz Uvolnit do skladu na stránce Pracovní plocha plánování nákladu

- Logika byla upravena tak, aby používala aplikované zásady konsolidace.
- Dodávky jsou nyní konsolidovány pouze v rámci jednoho nákladu.

### <a name="consolidate-shipments-page"></a>Stránka konsolidace dodávek

- Hledání podobných dodávek (to znamená kandidátů na konsolidaci) bylo změněno tak, že používá pole vybraná v zásadě konsolidace dodávek.
- Pole, která mají různé hodnoty v různých dodávkách, jsou nyní nastavena na prázdná. (Dříve byly použity hodnoty z vybrané „základní“ dodávky.)

### <a name="shipment-consolidation-workbench-page"></a>Stránka pracovní plochy konsolidace dodávek

- Nová funkce replikuje proces ruční konsolidace ve větším měřítku.
- Nyní můžete tuto stránku otevřít z nabídky **Uvolnění do skladu** v modulu **Řízení skladu**.
- Algoritmus analyzuje stávající dodávky, které ještě nebyly expedovány. Poté navrhuje konsolidaci na základě polí, která jsou vybrána v zásadách konsolidace.

## <a name="comparison-of-functionality"></a>Porovnání funkcí

Následující tabulka shrnuje, jak funguje konsolidace dodávek, když nepoužíváte zásady konsolidace dodávek a když je používáte.

| Bez zásad konsolidace dodávek | Se zásadami konsolidace dodávek |
|---|----|
| Nelze použít | Prodej nebo převod dodávek vybraných pro konsolidaci musí mít stejnou zásadu konsolidace jako dodávka, která se vytváří, nebo musí být přiřazeny k otevřené dodávce (když je zapnutá možnost **Konsolidovat se stávajícími dodávkami**). |
| Postup *Uvolnění do skladu* nehledá mezi existujícími dodávkami, aby nalezl dodávku pro konsolidaci. Pouze dodávky, které jsou vytvořeny aktuální instancí postupu *Uvolnění do skladu* se používá k nalezení dodávky pro konsolidaci. | Pokud je zapnuta možnost **Konsolidovat se stávajícími dodávkami** pro zásadu konsolidace, která se aktuálně používá, vyhledává proces *Uvolnění do skladu* mezi stávajícími dodávkami, které byly vytvořeny na základě stejné zásady konsolidace, aby našel dodávku pro konsolidaci. Pokud tedy máte dvě zásady, dodávka, která se vytváří na základě zásady 2, nebude nikdy konsolidována s dodávkou, která byla vytvořena na základě zásady 1. |
| Nelze použít | Pokud je seznam polí zásad konsolidace prázdný nebo pokud zásadu nelze najít, vytvoří se pro každou prodejní objednávku nebo řádek převodního příkazu nová dodávka. |
| Následující pole konsolidace definuje jedinečnou kombinaci hodnot, která se používá ke konsolidaci dodávek pro *řádek převodního příkazu*. (Všechna ostatní pole jsou ignorována.)<ul><li>Číslo objednávky (OrderNum)</li></ul> | Následující pole konsolidace definují jedinečnou kombinaci hodnot, která se používá ke konsolidaci dodávek pro *řádek převodního příkazu*. (Všechna ostatní pole jsou ignorována.)<ul><li>Číslo objednávky (OrderNum)</li><li>Příjemce dodávky (DeliveryName)</li><li>Poštovní adresa (DeliveryPostalAddress)</li><li>ISO kód země (CountryRegionISOCode)</li><li>Adresa (Address)</li><li>Pracoviště (InventSiteId)</li><li>Sklad (InventLocationId)</li><li>Dopravce dodávky (CarrierCode)</li><li>Služba přepravce (CarrierServiceCode)</li><li>Způsob dodání (ModeCode)</li><li>Skupina přepravců (CarrierGroupCode)</li><li>Dodací podmínky (DlvTermId)</li></ul>Tato pole jsou jediná pole, která jsou k dispozici a inicializovaná při vytvoření nové dodávky. |
| Následující pole konsolidace definují jedinečnou kombinaci hodnot, která se používá ke konsolidaci dodávek pro *řádek prodejní objednávky*. (Všechna ostatní pole jsou ignorována.)<ul><li>Číslo objednávky (OrderNum)</li><li>Reference zákazníka (CustomerRef)</li><li>Požadavek zákazníka (CustomerReq)</li><li>Dodací podmínky (DlvTermId)</li></ul> | Následující pole konsolidace definují jedinečnou kombinaci hodnot, která se používá ke konsolidaci dodávek pro *řádek prodejní objednávky*. (Všechna ostatní pole jsou ignorována.)<ul><li>Číslo objednávky (OrderNum)</li><li>Číslo účtu (AccountNum)</li><li>Příjemce dodávky (DeliveryName)</li><li>Poštovní adresa (DeliveryPostalAddress)</li><li>ISO kód země (CountryRegionISOCode)</li><li>Adresa (Address)</li><li>Pracoviště (InventSiteId)</li><li>Sklad (InventLocationId)</li><li>Dopravce dodávky (CarrierCode)</li><li>Služba přepravce (CarrierServiceCode)</li><li>Způsob dodání (ModeCode)</li><li>Skupina přepravců (CarrierGroupCode)</li><li>ID zprostředkovatele (BrokerCode)</li><li>Směr (LoadDirection)</li><li>Dodací podmínky (DlvTermId)</li><li>Reference zákazníka (CustomerRef)</li><li>Požadavek zákazníka (CustomerReq)</li></ul>Tato pole jsou jediná pole, která jsou k dispozici a inicializovaná při vytvoření nové dodávky. |
| Nelze použít | Následující pole konsolidace jsou povinná pro *řádek prodeje* a nelze je odstranit:<ul><li>Číslo účtu (AccountNum)</li><li>Příjemce dodávky (DeliveryName)</li><li>Poštovní adresa (DeliveryPostalAddress)</li><li>Sklad (InventLocationId)</li></ul>Ve výchozím nastavení budou tato pole přiřazena při vytvoření nové zásady. Nelze je odstranit. |
| Postup *Uvolnění nákladu do skladu* na stránce **Pracovní plocha plánování nákladu** používá svůj vlastní samostatný kód k vytváření dodávek a vln. | Zásady konsolidace dodávek se používají k určení polí, která by měla být vyhodnocena pro konsolidaci. Dodávky jsou konsolidovány pouze v rámci jednoho nákladu. |
| Ručně vyberete **Konsolidujte dodávek** na stránce **Všechny dodávky** a poté vyberte cílovou „základní“ dodávku. Filtr navrhne všechny existující dodávky, které mají shodné hodnoty pro několik klíčových polí. | Ručně vyberete **Konsolidujte dodávek** na stránce **Všechny dodávky** a poté vyberte cílovou „základní“ dodávku. Systém navrhne další existující dodávky spárováním hodnot několika klíčových polí, která jsou nakonfigurována pro příslušné zásady konsolidace dodávek. |
| Můžete použít příkaz **Konsolidovat dodávky** na stránce **Všechny zásilky** pouze pro jednu dodávku. | Stránka **Pracovní plocha konsolidace dodávek** vám pomůže najít sadu dodávek, které ještě nejsou v expedovaném stavu. Tyto dodávky jsou analyzovány na základě několika klíčových polí, která jsou nakonfigurována v zásadách konsolidace dodávek. Všechny dodávky, u nichž se hodnoty těchto polí shodují, jsou navrženy ke konsolidaci.<p>Konsolidaci můžete ručně udržovat odebráním dodávek z navrhovaných konsolidací nebo přidáním dodávek k nim. Může nastat několik typů chyb, některé však můžete přepsat.</p> |
| **Poznámka k návrhu:** Postup *Automatické uvolnění prodejních objednávek do skladu* rozdělí řádky prodeje do skupin. Každá skupina má svou vlastní jedinečnou hodnutu **ReleaseToWarehouseId** a zpracovává je samostatně postupem *Uvolnění do skladu*. Tento postup vytvoří novou práci bez ohledu na nastavení pracovní přestávky. | **Poznámka k návrhu:** Postup *Automatické uvolnění prodejních objednávek do skladu* přiřadí stejnou hodnotu **ReleaseToWarehouseId** pro všechny zpracovávané řádky prodeje. Všechny řádky prodeje jsou zpracovávány postupem *Uvolnění do skladu* současně. Chcete-li zajistit dřívější chování, musíte nakonfigurovat pracovní přestávku podle ID dodávky. |

## <a name="additional-resources"></a>Další prostředky

- [Konfigurace zásad konsolidace dodávek](configure-shipment-consolidation-policies.md)
