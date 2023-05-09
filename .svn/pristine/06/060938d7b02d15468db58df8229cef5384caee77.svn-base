package cloud.bluetea.mapper;

import java.util.Date;

import org.junit.Test;
import org.junit.runner.RunWith;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.test.context.ContextConfiguration;
import org.springframework.test.context.junit4.SpringJUnit4ClassRunner;

import lombok.extern.log4j.Log4j;

@RunWith(SpringJUnit4ClassRunner.class)
@ContextConfiguration("file:src/main/webapp/WEB-INF/spring/root-context.xml")
@Log4j
public class TicketMapperTests {
	
	@Autowired
	TicketMapper ticketMapper;
	
	@Test
	public void testDeleteTicket() {
		ticketMapper.deleteTicket(3L);
	}
	// 영화정보번호에 따른 영화 티켓 조회
    @Test
    public void testGetListTicketCinema() {
        log.info(ticketMapper.getListTicketCinema(54));
    }

    // memberid에 따른 영화티켓 조회
    @Test
    private void testMemberIdSelectOne() {
        log.info(ticketMapper.memberIdSelectOne("userid"));
    }

    // 영화정보번호에 따른 1개 조회
    @Test
    private void testctnoSelectOne() {
        log.info(ticketMapper.ctnoSelectOne(1L));
    }

    // 영화티켓예약일에 따른 티켓 조회
    @Test
    private void testRegdateSelectOne() {
        ticketMapper.regdateSelectOne(new Date());
    }

    // 좌석에 따른 티켓 조회
    @Test
    private void testSeatSelectOne() {
        ticketMapper.seatSelectOne(0, 0);
    }

}