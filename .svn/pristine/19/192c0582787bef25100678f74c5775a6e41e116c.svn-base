package cloud.bluetea.persistence;

import static org.junit.Assert.assertNotNull;

import java.sql.Connection;
import java.sql.DriverManager;

import javax.sql.DataSource;

import org.junit.Test;
import org.junit.runner.RunWith;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.test.context.ContextConfiguration;
import org.springframework.test.context.junit4.SpringJUnit4ClassRunner;

import lombok.extern.log4j.Log4j;

/**
 * packageName    : cloud.bluetea.persistence (패키지명)
 * fileName       : JDBCTests (파일명)
 * author         : 우성준 (작성자)
 * date           : 2023/04/03 (생성일 또는 최종 수정일)
 * description    : JDBC 연결 테스트  (파일 목적)
 * ===========================================================
 * DATE              AUTHOR             NOTE
 * -----------------------------------------------------------
 * 2023/04/03        우성준           파일생성
 *
 * 
 * 
 */

@RunWith(SpringJUnit4ClassRunner.class)
@ContextConfiguration("file:src/main/webapp/WEB-INF/spring/root-context.xml")
@Log4j
public class JDBCTests {
	@Autowired
	private DataSource dataSource;

	@Test
	public void testConnection() {
		try(Connection conn = DriverManager.getConnection("jdbc:mariadb://np.flatjava.co.kr:3306/semi","sample","1234")) {
			log.info(conn);
		} catch (Exception e) {
			// TODO: handle exception
		}
	}
	
	@Test
	public void testDataSource() {
		assertNotNull(dataSource);
		try {
			log.info(dataSource.getConnection());
		}
		catch (Exception e) {
			// TODO: handle exception
			e.printStackTrace();
		}
	}
}
