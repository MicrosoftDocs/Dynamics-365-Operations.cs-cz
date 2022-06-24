---
title: Konfigurace parametrů aplikace Human Resources
description: Tento článek vysvětluje, jak nastavit parametry specifické pro společnost v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dd645dcc79672e7f69afe47b803b90a04c22305d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856273"
---
# <a name="configure-human-resources-parameters"></a>Konfigurace parametrů aplikace Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Nastavení některých parametrů lidských zdrojů nesmí být sdílena napříč společnostmi, zatímco nastavení jiných parametrů jsou specifické pro společnost. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů specifické pro společnost.

K nastavení parametrů lidských zdrojů slouží dvě stránky. Pro parametry, které jsou sdíleny napříč společnostmi, použijte stránku **Sdílené parametry lidských zdrojů**. Pro parametry, které jsou specifické pro společnost (jinými slovy nastavení se použije pro jednu společnost), můžete použít stránku **Parametry lidských zdrojů**.

![Přechod na parametry lidských zdrojů.](./media/hr-employee-self-service-human-resources-parameters.png)

Na stránce **Parametry lidských zdrojů** jsou nastavení rozdělena mezi šest karet:

- **Obecný**
- **Nábor** (tato karta není součástí Dynamics 365 Human Resources)
- **Kompenzace**
- **Číselné řady**
- **Pracovní volno**
- **Samoobsluha pro zaměstnance**
- **Samoobsluha pro manažery**
- **Správa zaměstnaneckých výhod**
- **Pracovní volno a absence**
- **Způsoby platby**

Každá karta obsahuje informace, které se vztahují na jednu společnost.

## <a name="general"></a>Obecný

Nastavení kartě **Obecné** určuje vzhled informací o absencích, zraněních a onemocněních a nově přijatých zaměstnancích. Nastavení na této kartě také definují některé výchozí položky, které se zobrazí při práci. Tato karta konkrétně umožňuje:

- Vybrat barvu, kterou chcete použít na otevřené transakce absencí.
- Určit šablonu stylů, kterou chcete použít pro sestavy.
- Povolit integraci mezi školeními a registrací absencí.
- Vybrat kód absence, který se používá k řízení této integrace.
- Uvést, jak dlouho chcete zachovat případy zranění a nemoci.
- Zadat výchozí identifikační číslo zobrazené při najímání nového pracovníka.
- Zadejte datum, které se použije k výpočtu let služby. 

![Karta Obecné.](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Nábor

Nastavení na kartě **Nábor** definují typy dokumentů používané pro korespondenci automaticky zasílanou uchazečům. Můžete také uvést náborový projekt používaný pro nevyžádané přihlášky.

Období definované pro **Náborový projekt časově určuje**, které náborové projekty jsou zahrnuty na dlaždici **Časové projekty** v pracovním prostoru **Řízení náboru**. Období, které je definováno pro upozornění na termín přihlášky slouží k zobrazení náborových projektů, kterým se blíží jejich konečný termín přihlášky na dlaždici **Blíží se termín přihlášky** v pracovním prostoru **Nábor**.

Další informace o náboru najdete na stránce [Nábor uchazečů o práci](hr-personnel-recruit.md).

## <a name="compensation"></a>Kompenzace

V aplikaci Dynamics 365 Finance definuje nastavení na kartě **Kompenzace**, zda uživatelé musí potvrzovat, že chtějí uložit informace pro plán fixní nebo variabilní kompenzace. Vyberete-li možnost **Povolit ověření ukládání**, obdrží uživatelé zprávu s dotazem, zda chtějí uložit záznam, kdykoli zavřou stránku související s kompenzacemi, . Některé stránky ve Správě kompenzací neumožní uživatelům odstranit informace. Vyzváním uživatelů k ověření, zda chtějí informace ukládat, budete schopni omezit informace, které jsou ukládány, a později nejdou odstranit. Pokud zrušíte zaškrtnutí možnosti **Povolit ověření ukládání**, záznamy jsou uloženy okamžitě, možná ještě předtím, než je uživatel připraven. Pokud používáte funkci Řízení výkonnosti, můžete na kartě **Kompenzace** vybrat model hodnocení, který má být použit namísto modelu přiřazeného k plánům kompenzace při hodnocení výkonnosti.

V Human Resources můžete na kartě **Kompenzace** omezit přístup k plánům kompenzace a nastavit výchozí měnu.

Další informace o kompenzacích naleznete v tématu [Přehled plánů kompenzací](hr-compensation-overview.md).

![Karta Kompenzace.](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>Číselné řady

Nastavení na kartě **Číselná řada** určuje posloupnosti používané k automatickému přiřazování ID k položkám v Human Resources, například:

- Žádosti
- Registrace absencí
- Výsledky procesu kompenzace
- Čísla případů
- Kurzy
- Agendy kurzů

Spravovat odkazy číselných řad a kódy můžete na stránce se seznamem **Číselné řady** (vyberete **Správa organizace > Číselné řady > Číselné řady**).

Další informace naleznete v tématu [Přehled číselných řad](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Počet hodin, které jsou odpracovány nesmí překročit 1 250 a délka zaměstnání nesmí přesáhnout 12 měsíců. Tyto maximální hodnoty jsou v souladu s federálním právem ve Spojených státech amerických.

![Karta Číselné řady.](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>Pracovní volno

Na kartě Pracovní volno nastavíte požadavky na způsobilost a hodiny nároků na pracovní volno. Další informace naleznete v tématu [Konfigurace parametrů pracovního volna a absence](hr-leave-and-absence-parameters.md).

![Karta Pracovní volno.](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Samoobsluha pro zaměstnance

Nastavení na kartě **Samoobsluha pro zaměstnance** ovlivňuje, jak se zaměstnancům zobrazuje jejich **samoobsluha**. Na této kartě můžete provést následující úkoly:

- Zapsat název pracovního prostoru **Samoobsluha pro zaměstnance**
- Vybrat, jaké informace může manažer pro zaměstnance zadat
- Přidat užitečné odkazy pro zaměstnance
- U zaměstnanců můžete omezit jejich schopnost přidávat nebo upravovat detaily kontaktních údajů. Další informace najdete v tématu [Omezení úpravy osobních údajů](hr-employee-self-service-restrict-editing.md).

Další informace o nastavení **samoobsluhy pro zaměstnance** najdete v části [Přehled samoobsluhy pro zaměstnance a manažera](hr-employee-manager-self-service-overview.md).

![Karta Samoobsluha pro zaměstnance.](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Samoobsluha pro manažery

Nastavení na kartě **Samoobsluha pro manažery** ovlivní to, co manažeři uvidí ve své **samoobsluze**. Na této kartě můžete konfigurovat následující možnosti:

- Rozsah pro vypršení platnosti záznamů
- Zda mohou manažeři informací prohlížet záznamy, jejichž platnost vyprší
- Zda mohou manažeři zobrazit otevřené pozice pro další podřízené
- Pohledy na odcházející pracovníky
- Užitečné odkazy pro manažery

Další informace o nastavení **samoobsluhy pro manažery** najdete v části [Přehled samoobsluhy pro zaměstnance a manažera](hr-employee-manager-self-service-overview.md).

![Karta Samoobsluha pro manažery.](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Správa zaměstnaneckých výhod

Na kartě **Správa výhod** můžete konfigurovat e-mailové možnosti pro správu výhod. Další informace o nastavení a použití správy zaměstnaneckých výhod naleznete v tématu [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).

![Karta Správa zaměstnaneckých výhod.](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Pracovní volno a absence

Další informace o nastavení a používání pracovního volna a absencí získáte v části [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Způsoby platby

Na kartě **Metody platby** můžete vybrat metody platby podporované vaší organizací. Další informace o konfiguraci kompenzací naleznete v tématu [Přehled plánů kompenzací](hr-compensation-overview.md).

![Karta Metody platby.](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
